[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/pkfln/mta-discord-rpc">
    <img src="assets/mtasa.png" alt="Logo" width="128" height="128">
  </a>

  <h3 align="center">MTA HD Community</h3>

  <p align="center">
    External Rich Presence Manager for Multi Theft Auto: San Andreas.
    <br />
    <br />
    <a href="https://github.com/pkfln/mta-discord-rpc/issues">Report an issue</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [Installation](#installation)
  * [Testing](#testing)
  * [Installing](#installing)
  * [Updating](#updating)
* [Why?](#why)
* [Adding server assets](#adding-server-assets)
* [Troubleshooting](#troubleshooting)
  * [Discord shows "Grand Theft Auto: San Andreas" as my current game](#discord-shows-grand-theft-auto-san-andreas-as-my-current-game)
  * [Discord shows "MTA: San Andreas" as my current game](#discord-shows-mta-san-andreas-as-my-current-game)
  * [Rich presence is not showing MTA anymore, eventhough I restarted MTA multiple times already](#rich-presence-is-not-showing-mta-anymore-eventhough-i-restarted-mta-multiple-times-already)
* [Contributing](#contributing)
* [Known bugs](#known-bugs)
* [License](#license)



<!-- INSTALLATION -->
## Installation

### Testing

First make sure it works for you before you install it. **It's recommended to be on the latest Windows 10 Build (I haven't tested it on any other OS or earlier versions of Windows).**
You will also need to play MTA:SA through its proxy application, so Discord doesn't pickup default GTA:SA as the current playing game.
1. Make sure your MTA:SA uses proxy_sa.exe instead of gta_sa.exe. To check this, open your Task Manager and see which one of both applications is running while you have MTA:SA open. Click [here](#discord-shows-grand-theft-auto-san-andreas-as-my-current-game) to learn how to force this behaviour.
2. Close your MTA:SA instance if you have it running.
3. Download the newest release from the <a href="https://github.com/pkfln/mta-discord-rpc/releases">releases page</a> (mta-discord-rpc.exe).
4. Open the folder containing the downloaded executable.
5. Execute the file by double-clicking it.
6. If you're not getting any errors, try to open MTA:SA.
7. Check your Discord Rich Presence status and see, if it's setting your status.
8. If everything works so far, you're ready to install it. If you do get some errors, try to fix them or open a new issue. Also don't forget to check the [Troubleshooting](#troubleshooting) section.

### Installing

1. Press <kbd>Win</kbd> + <kbd>R</kbd>, you should then see the Run window.
2. Type in `shell:startup` and press <kbd>Enter</kbd>.
3. Either create a shortcut to the executable you just downloaded or move it into this new folder window.
4. Next time you login to your Windows, mta-discord-rpc will automatically start.

To uninstall it / disable it from the Windows startup, simply delete the downloaded executable or the shortcut you created.

### Updating
To update, just download the latest build from the <a href="https://github.com/pkfln/mta-discord-rpc/releases">releases page</a> and repeat the installation process.



<!-- WHY -->
## Why?

Since you can't really make clientsided modifications for MTA (or at least not that I know of), I decided to do it this way, so that it doesn't interfer with the actual process and is fully external. MTA had rich presence support in the past, but it got removed for some reason.



<!-- ADDING SERVER ASSETS -->
## Adding server assets

If you want your server logo to be shown on the rich presence instead of the default MTA logo, create a pull request with your server logo.
1. Fork this project
2. Create your branch (e.g. asset/my-server): `git checkout -b asset/my-server`
3. Add your server logo in the assets directory. Make sure your logo has a background and a minimum size of 512x512 (1024x1024 recommended). Only PNGs are currently supported. Name your file in the following format: `[ip]_[port].png` (no hostnames).
4. Stage your file: `git add assets/154.208.140.95_22005.png`
4. Commit your changes: `git commit -m 'Add server logo for Localhost'`
5. Push your new changes: `git push origin asset/my-server`
6. Open a Pull Request



<!-- TROUBLESHOOTING -->
## Troubleshooting

### Discord shows "Grand Theft Auto: San Andreas" as my current game

You must force MTA:SA to use their proxy application. The easiest method probably is installing an ASI loader: <a href="https://www.gtagarage.com/mods/show.php?id=21709">Download Silent's ASI Loader here</a> and add & replace these files to your GTA:SA directory.


### Discord shows "MTA: San Andreas" as my current game

You probably added it manually to your Game Activity detection list. Remove it from there in the Discord settings.


### Rich presence is not showing MTA anymore, eventhough I restarted MTA multiple times already

Logout from Windows & log back in, that should fix it.



<!-- CONTRIBUTING -->
## Contributing

Coming soon.



<!-- KNOWN BUGS -->
## Known bugs

- Having multiple Discord instances open won't display the rich presence



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.






<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/pkfln/mta-discord-rpc.svg?style=flat-square
[contributors-url]: https://github.com/pkfln/mta-discord-rpc/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/pkfln/mta-discord-rpc.svg?style=flat-square
[forks-url]: https://github.com/pkfln/mta-discord-rpc/network/members
[stars-shield]: https://img.shields.io/github/stars/pkfln/mta-discord-rpc.svg?style=flat-square
[stars-url]: https://github.com/pkfln/mta-discord-rpc/stargazers
[issues-shield]: https://img.shields.io/github/issues/pkfln/mta-discord-rpc.svg?style=flat-square
[issues-url]: https://github.com/pkfln/mta-discord-rpc/issues
[license-shield]: https://img.shields.io/github/license/pkfln/mta-discord-rpc.svg?style=flat-square
[license-url]: https://github.com/pkfln/mta-discord-rpc/blob/master/LICENSE
