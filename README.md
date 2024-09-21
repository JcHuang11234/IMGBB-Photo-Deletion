
# Selenium Automation Script for Deleting Photos on imgbb

This Python script automates the process of deleting multiple photos from your imgbb account using Selenium and the Firefox web driver. The script logs into your account, selects photos in batches, and deletes them until the specified number of photos are deleted.

## Requirements

- Python 3.x
- Selenium
- GeckoDriver (Firefox WebDriver)
- Firefox browser installed

### Python Dependencies

You can install the necessary Python packages using the following command:

```bash
pip install selenium
```

## Setup

1. **Install GeckoDriver:**
   Download the GeckoDriver from the official repository: https://github.com/mozilla/geckodriver/releases.
   Make sure to add GeckoDriver to your system's PATH.

2. **Install Python Packages:**
   Ensure you have Selenium installed. If not, you can install it using `pip`:

   ```bash
   pip install selenium
   ```

3. **Firefox Browser:**
   This script uses Firefox as the browser. Ensure Firefox is installed on your system.

## Usage

1. **Clone or download this repository:**

   ```bash
   git clone https://github.com/JcHuang11234/IMGBB-Photo-Deletion.git
   ```

2. **Modify the script:**

   Open the Python script in your preferred editor and update the following fields with your login credentials:

   ```python
   email_field.send_keys("YOUR-EMAIL-ADDRESS")
   password_field.send_keys("YOUR-PASSWORD")
   ```

3. **Run the script:**

   Run the Python script with the following command:

   ```bash
   python delete_photos_imgbb.py
   ```

4. **Input the number of photos to delete:**

   When prompted, enter the total number of photos you want to delete from your imgbb account.

   Example:

   ```bash
   Enter the total number of photos you want to delete: 100
   ```

## How it Works

- The script logs into your imgbb account using your email and password.
- It iterates through batches of photos (32 per batch), selects them, and deletes them.
- The script automatically calculates the number of iterations required based on the total number of photos you want to delete.
- In case of errors during deletion, the page is refreshed and the process retries.

## Known Issues

- If imgbb changes its HTML structure, the XPath selectors in the script might break. You will need to update the XPaths accordingly.
- Ensure a stable internet connection for the script to run smoothly, as refreshing and waiting times are hardcoded.

## Customization

- **Headless Mode:** If you want to run the script without opening the browser window, set the `headless` option to `True` in the following line:

   ```python
   options.headless = True
   ```

- **Delays:** The script includes `time.sleep()` to allow the page to load properly before each action. You can modify these delays if needed.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
