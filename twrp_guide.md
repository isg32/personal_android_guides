# Installing Dependencies
```bash
sudo apt-get install git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z1-dev ccache libgl1-mesa-dev libxml2-utils xsltproc unzip python
```

# Download TWRP source:
```bash
mkdir twrp && cd twrp
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-12.1
repo sync
```
# get your device repo
> git clone device_repo_url device / manufacturer / device_codename
```bash
git clone https://github.com/twrpdtgen/android_device_motorola_coful/ device/motorola/coful
```
# sauce it
```bash
source build/envsetup.sh
```
# lunch it
> lunch omni_<device_codename>-eng
```bash
lunch omni_coful-eng
```
# start build
```bash
mka recoveryimage
```
