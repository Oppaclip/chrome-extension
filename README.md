# OppaClip Cookie Helper

A simple Chrome Extension to extract specific YouTube cookies (including `HttpOnly` ones) and export them in the Netscape HTTP Cookie File format required by `yt-dlp`.

This tool helps solve the "Sign in to confirm you're not a bot" error by allowing you to easily export your authenticated session cookies.

## Installation

1.  Open Google Chrome.
2.  Navigate to `chrome://extensions/` in the address bar.
3.  Enable **Developer mode** by toggling the switch in the top-right corner.
4.  Click the **Load unpacked** button in the top-left corner.
5.  Select this folder (`chrome-extension`) from your file explorer.

## Usage

1.  Go to [YouTube.com](https://www.youtube.com) and ensure you are logged in to the account you want to use.
2.  Click the **Extensions** icon (puzzle piece) in the Chrome toolbar.
3.  Select **OppaClip Cookie Helper**.
4.  Click the red **Download cookies.txt** button.
5.  A `cookies.txt` file will be downloaded to your computer.

## Using with OppaClip Server

1.  Upload the downloaded `cookies.txt` to your server.
    ```bash
    scp cookies.txt <your-server-user>@<your-server-ip>:/home/ubuntu/cookies.txt
    ```
2.  The application will automatically pick up the new cookies (since we enabled hot-swapping via volume mount). No restart required.
