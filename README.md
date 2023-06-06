# siimple-url-check-python-script
URL Checker
This script allows you to check the validity and accessibility of a given URL.

Prerequisites
Before running this script, make sure you have the following installed:

Python (version 3 or above)
Requests library (pip install requests)
Usage
Import the necessary module:

python
Copy code
import requests
Define the check_url function:

python
Copy code
def check_url(url):
    try:
        response = requests.get(url)
        if response.status_code == 200:
            print(f"URL {url} is valid and accessible.")
        else:
            print(f"URL {url} returned a non-200 status code: {response.status_code}")
    except requests.exceptions.RequestException as e:
        print(f"An error occurred while checking URL {url}: {str(e)}")
Use the function to check URLs:

python
Copy code
check_url("https://www.google.com")
check_url("https://www.yahoo.com")
Replace the URLs in the check_url function with the ones you want to check.

Example
Here's an example of how to use the check_url function:

python
Copy code
check_url("https://www.google.com")
check_url("https://www.yahoo.com")
Output:

arduino
Copy code
URL https://www.google.com is valid and accessible.
URL https://www.yahoo.com is valid and accessible.
Error Handling
If an error occurs during the URL check, the script will print an error message.

Contributing
Contributions are welcome! If you find any issues or have suggestions, please open an issue or submit a pull request.
