# Asahi Fedora Remix Local Mirror

This project is basically a script which pre-fetches assets allowing the Asahi Fedora installer to run without repeatedly fetching assets from a remote CDN. Note however that network access is still required to successfully bless the boot volume at the end of the install process.

## Usage

1. Clone the repo at `/opt/asahi-fedora-remix`
2. Run `/opt/asahi-fedora-remix/mirror` to download install media and IPSW firmware images

    After this has run, the file tree should look something like this:
    
    ```shell
    /opt/asahi-fedora-remix
    ├── LICENSE
    ├── README.md
    ├── install
    ├── installer-v0.5.3.tar.gz
    ├── installer_data.json
    ├── installer_latest
    ├── ipsw
    │   └── UniversalMac_12.3_21E230_Restore.ipsw
    ├── mirror
    └── os
        ├── fedora-38-20230405.zip
        ├── fedora-38-kde-20230405.zip
        ├── fedora-38-minimal-20230405.zip
        └── fedora-38-server-20230405.zip
    ```

3. Run `/opt/asahi-fedora-remix/install` to start the installation

    This is the equivalent of running `curl -s https://asahi-fedora-remix.org/install | sh` but will instead utilize the assets stored locally for installation.

## License

This work is licensed under the MIT license. See [LICENSE](https://github.com/davidalger/asahi-fedora-remix/blob/main/LICENSE) file for details.
