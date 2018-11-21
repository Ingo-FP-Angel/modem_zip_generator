# Fairphone 2 `modem.zip`
Update the proprietary firmware of your [Fairphone 2](https://shop.fairphone.com) to the latest available. Fairphone updates the software of the Fairphone 2 with [security patches](https://source.android.com/security/bulletin/) on a monthly basis.

This repo host the code to generate a reproducible, flashable ZIP file (called `modem.zip`) with the latest proprietary firmware from a recent Fairphone OS or Fairphone Open OTA.

### Download
You can always download the latest `modem.zip` directly from [here](https://io.pinterjann.is/public/misc/fairphone/modem/modem-latest.zip). Alternatively, you can get them at the [releases page at GitHub](https://github.com/WeAreFairphone/modem_zip_generator/releases).

### System requirements
The following tools are required for the script to run:
 - GNU `make`
 - `bash`
 - `curl`
 - `zip` & `unzip`
 - `sha256sum`

The project has been developed on GNU/Linux systems, it should however run on other UNIX systems, too. For Mac OS you'll need the GNU coreutils. Using [Homebrew](https://brew.sh): `$ brew install coreutils`.


### Build
Clone the repository and execute `make build`, it will download and verify the official Fairphone 2 firmware images and extract the proprietary firmware images.

If you want to test your changes, just run `make install` and connect your device in recovery mode and sideload to your computer.

To make a release, just execute `make release`. It will output a `modem-{VERSION}_YYYY-MM-DD.zip` to the `release/` folder.

### Contributing
We welcome contributions to this project, specially for new releases. We do this on our free time and we can fall behind the security releases schedule of Fairphone. [Fork this repo](https://github.com/WeAreFairphone/modem_zip_generator/fork), commit your changes —usually tweaking the top of the `Makefile`— and [open a pull request](https://github.com/WeAreFairphone/modem_zip_generator/pull/new).

You can find useful this links:
 - Fairphone Open update files can be found at https://code.fairphone.com/projects/fp-osos/user/fairphone-open-source-os-downloads.html
 - Fairphone OS update files can be found at https://support.fairphone.com/hc/en-us/articles/213290023-Fairphone-OS-downloads-for-Fairphone-2

### Misc
See this [forum post](https://forum.fairphone.com/t/pencil2-fp2-modem-firmware/35374) for more information about this project.
