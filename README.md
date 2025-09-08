# _Yandex-Browser-for-Void-Linux ![void](https://github.com/sofijacom/yandex-browser/assets/107557749/0cb14595-dcea-4f79-84a4-0185b1df379d)_


![2024-09-24_22-23](https://github.com/user-attachments/assets/4d556c6b-a092-44f2-b2e1-1e9dce9af76d)


### Installation

Clone `void-packages` and install the environment for building packages:
```
git clone https://github.com/void-linux/void-packages.git
cd void-packages
./xbps-src binary-bootstrap
```

To collect a package marked "restricted":
```
echo "XBPS_ALLOW_RESTRICTED=yes" >> etc/conf
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
sudo xbps-install -v --repository hostdir/binpkgs/nonfree yandex-browser
```

Install codec:
```
sudo rm "/opt/yandex/browser/libffmpeg.so"
```
```
sudo /opt/yandex/browser/update_codecs /opt/yandex/browser || true
```
