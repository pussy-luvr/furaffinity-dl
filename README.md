# FurAffinity Downloader
**furaffinity-dl** is a bash script for batch downloading of galleries and favorites from furaffinity.net users.
I've written it for preservation of culture, to counter the people nuking their galleries every once a while.

Supports all known submission types: images, texts and audio. Sorts downloaded files in chronological order.
I'd like to eventually expand it to download the description pages as well. Patches are welcome!

**furaffinity-batch-dl** is a simple rubber for furaffinity-dl which lets you easily 
snapshot multiple galleries at once from a username list file.

## Requirements

Coreutils, bash and wget are the only dependencies.

furaffinity-dl was tested only on Linux. It should also work on Mac and BSDs.
Windows users can probably get it to work via Cygwin or Microsoft's "BASH on Windows", but running a virtual machine with Linux might be simpler.

## Usage

### furaffinity-dl
 `furaffinity-dl section/username`

All files from the given section and user will be downloaded to the current directory.

#### Examples
 `furaffinity-dl gallery/kodardragon`

 `furaffinity-dl scraps/---`

 `furaffinity-dl favorites/kivuli`

You can also log in to download restricted content. To do that, log in to FurAffinity in your web browser, export cookies to a file from your web browser in Netscape format (there are extensions to do that [for Firefox](https://addons.mozilla.org/en-US/firefox/addon/export-cookies/) and [for Chrome/Vivaldi](https://addons.mozilla.org/en-US/firefox/addon/export-cookies/)) and pass them to the script as a second parameter, like this:

 `furaffinity-dl gallery/gonnaneedabiggerboat /path/to/your/cookies.txt`

### furaffinity-batch-dl

 `furaffinity-batch-dl`

Loads `cookies.txt` and a user-created `usernames.txt` with one username on each line to create a 
gallery snapshot for multiple artists. `cookies.txt` and `username.txt` must be in the same 
directory as the bash scripts. Each subsequent use creates a new timestamped directory in 
the current directory.

## TODO
 * Download author's description of the artwork, and ideally the entire description page along with user comments

## Disclaimer
It is your own responsibility to check whether batch downloading is allowed by FurAffinity terms of service and to abide by them. For further disclaimers see LICENSE.

## See also

There is a similar downloader for VCL art library, see https://github.com/Shnatsel/vcl-dl
