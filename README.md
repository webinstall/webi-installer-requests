# webi-installer-requests

This is just to house issues for requests for new Webi installers.

# How to create a webi installer

[![Video Tutorial: How to create a webi Installer](https://user-images.githubusercontent.com/122831/91064908-17f28100-e5ed-11ea-9cf0-ab3363cdf4f8.jpeg)](https://youtu.be/RDLyJtiyQHA)

This could be as simple as copying `_example`, updating the github releases
info, and doing a find and replace on a few file system path names.

## Skills required

- Basic Command Line knowledge (`mkdir`, `mv`, `ls`, `tar`, `unzip`, variables)

## Steps

1. Clone and setup the webi packages repo
   ```sh
   git clone git@github.com:webinstall/packages.git
   cd ./packages/
   npm install
   ```
2. Copy the example template and update with info from Official Releases:
   <https://github.com/___CHANGE/ME___/releases>
   ```sh
   rsync -av _example/ CHANGE-ME/
   ```
   - [ ] update `CHANGE-ME/release.js` to use the official repo
   - [ ] Learn how `CHANGE-ME` unpacks (i.e. as a single file? as a .tar.gz? as
         a .tar.gz with a folder named CHANGE-ME?)
   - [ ] find and replace to change the name
     - [ ] update `CHANGE-ME/install.sh` (see `bat` and `jq` as examples)
     - [ ] update `CHANGE-ME/install.ps1` (see `bat` and `jq` as examples)
3. Needs an updated tagline and cheat sheet
   - [ ] update `CHANGE-ME/README.md`
     - [ ] official URL
     - [ ] tagline
     - [ ] Switch versions
     - [ ] description / summary
     - [ ] General pointers on usage (and perhaps "gotchas")
