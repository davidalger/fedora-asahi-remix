# Asahi Fedora Remix Local Mirror

This project is basically a script which pre-fetches assets allowing the Asahi Fedora installer to run without repeatedly fetching assets from a remote CDN. Note however that network access is still required to successfully bless the boot volume at the end of the install process.

## Usage

1. Clone the repo at `/opt/asahi-fedora-remix`
2. Run `/opt/asahi-fedora-remix/mirror` to download install media and IPSW firmware images
3. Run `/opt/asahi-fedora-remix/install` to start the installation

    This is the equivalent of running `curl -s https://asahi-fedora-remix.org/install | sh` but will instead use the media now mirrored locally at `/opt/asahi-fedora-remix/os` and `/opt/asahi-fedora-remix/ipsw`.

## License

This work is licensed under the MIT license. See [LICENSE](https://github.com/davidalger/asahi-fedora-remix/blob/main/LICENSE) file for details.
