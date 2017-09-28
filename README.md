# getVmworld2017Videos - VMworld 2017 Video Downloader

Downloads the VMworld 2017 US & Europe Breakout Session videos.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine.

### Prerequisites

This script relies on the [YouTube-DL](https://rg3.github.io/youtube-dl/) Windows executable. Make sure that you download `youtube-dl.exe` into the same folder as this script. 

Here is an example PowerShell command that will download `youtube-dl.exe`.

```PowerShell
Invoke-WebRequest -Uri https://yt-dl.org/latest/youtube-dl.exe -OutFile youtube-dl.exe
```

### Installing

Make sure that you are in the directory that you want to download the videos,
and that you've already downloaded the prerequisite `youtube-dl.exe` file.

> **Note:** The videos will be downloaded in the highest resolution available.
 The total storage requirements of the videos is in the hundreds of Gigabytes.
 Make sure you have enough free space before running this script.

1. Download the `get-Vmworld2017Videos.ps1` script.

    ```PowerShell
    Invoke-WebRequest -Uri https://raw.githubusercontent.com/Dee76/getVmworld2017Videos/master/get-Vmworld2017Videos.ps1 -OutFile get-Vmworld2017Videos.ps1
    ```

2. Run the script.

    ```PowerShell
    get-Vmworld2017Videos.ps1
    ```

3. Sit back and watch the videos download. This will take _several_ minutes.

### Troubleshooting

If some videos fail to download, or the source Session video list is updated, simply run the script again. The list will be parsed and `youtube-dl.exe` will validate and skip any videos that were already successfully downloaded. Failed downloads will be resumed or restarted, and new videos downloaded.

## Built With

* [PowerShell](http://microsoft.com/powershell) - The scripting language used
* [YouTube-DL](https://rg3.github.io/youtube-dl/) - Dependency Management

## Authors

* **Dee Abson** - *Initial work* - [T.B.D.](https://teebeedee.org)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* Thanks to [William Lam](https://twitter.com/lamw) for putting the [session lists](https://github.com/lamw/vmworld2017-session-urls) together.
* Thanks to the vExpert Slack channel for the inspiration.
