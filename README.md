## Table of contents

- [About](#about)
- [Installation](#installation)
- [Usage](#usage)
  - [Advanced Usage](#advanced-usage)
- [Help](#help)

## About

This program exists to solve one problem: Provide a simple way to show an accurate sub point counter on stream that updates near real-time.

It interacts directly with the Twitch Dashboard and scrapes the numbers from there, then forwards those numbers to the companion to write it to a file you specify. The extension is inactive on all other webpages!

As a side note for those that aren't affiliates yet: anyone can use this program since it can also track followers!

## Installation

This program comes in two parts due to its unique construction.

The first part is a chrome extension (This works in anything that is chromium based!) which you can download [here](https://chrome.google.com/webstore/detail/twitch-sub-point-counter/khjdganpjdoeeinadcneikclmpcpbecd).

The second part is a windows application (sorry mac / linux users, porting this should be pretty simple, but its not as easy to package. Let me know if you need it!) which you can find the latest version of on the [releases page](https://github.com/ckohen/sub-counter-companion/releases) (It's the .msi not the source folder!).
* [Direct download link (v0.1.1)](https://github.com/ckohen/Sub-Counter-Companion/releases/download/v0.1.1/Sub_Counter_Companion_Installer.msi)

The program is a simple windows installer, and after installation it will behave like any other application. It does sit in your system tray however, so that you don't have to worry about it each time you start a stream.

## Usage

The extension is only active on the twitch dashboard, so head on over [there](https://twitch.tv/dashboard).

Once you are there, you can set up the extension by clicking on it in your toolbar.

Then:

1. Toggle your enabled state to on
2. Select which count you want to put in a file
3. Write some custom text in the output field. Wherever `$value` appears, it will be replaced with the selected count.
4. Set your update period to something that suits your needs. 
5. Make sure to save your changes!

For the application:

1. Open Twitch Sub Counter Companion (It will show up in the start menu!)
    - Note: it will open in tray by default
2. Double click the icon in the tray to open the application. (You can also right click -> Open)
3. Click `Select...` to select a text file to save in to. Settings in this app are saved automatically.

If you need to close the application for some reason, right click the taskbar icon then click exit. The `X` in the application will not quit it!

### Advanced Usage

By default, the app will start with windows. This can be changed in the right click menu of the taskbar icon.

You may have noticed that both the extension and the application have one additional option. This allows you to have a more complex setup.

For the application, the port number is the port it will listen on for incoming information the extension. It uses an HTTP request and custom API to do the updating, so if you ever find another way to get the data, you can still use this companion. The API will be documented at some point in the future.

Changing the port may be a good troubleshooting step, although it should be unnecessary.

On the extensions end, you can set a full custom url to send updates to, including the port. This can allow you to run the extension with your dashboard on one computer and the companion with obs on another computer! And again, if you feel like emulating the opposite API, you could rebuild it too!

## Help

If you have trouble understanding anything here or in the documentation, or if you are experiencing any type of problem, then you can contact me on discord! My tag is `ckohen#0013`. If discord doesn't work for you, you can also reach out to `ckohen@corncierge.com`.
