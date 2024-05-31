# _Yandex-Browser-for-Void-Linux ![void](https://github.com/sofijacom/yandex-browser/assets/107557749/0cb14595-dcea-4f79-84a4-0185b1df379d)_


### Installation

Clone `void-packages` and install the environment for building packages:
```
git clone https://github.com/void-linux/void-packages.git
cd void-packages
./xbps-src binary-bootstrap
```

To collect a package marked "restricted":
```
echo XBPS_ALLOW_RESTRICTED=yes >> etc/conf
```

Cloning the repository:
```
cd srcpkgs
git clone https://github.com/sofijacom/yandex-browser.git
cd ../
```

Assembling Yandex Browser:
```
./xbps-src pkg yandex-browser
```

Installing Yandex Browser:
```
xbps-install -v --repository hostdir/binpkgs/nonfree yandex-browser
```
