# maya-substance
## Install
### 1. Clone this source.
`cd /tmp`
#### Choose one:
#### A. Git HTTPS 
`git clone https://github.com/aaronrancsik/maya-substance-arch.git`
#### B. Git SSH 
`git clone git@github.com:aaronrancsik/maya-substance-arch.git`
### 2. Get the source zip.
`cd /tmp/maya-substance-arch`

`cp /tmp/maya20221_BIG/Packages/SubstanceInMaya-2.1.9-2022-Linux.rpm ./`
### 3. Create & install the package.
`makepkg -s`

`sudo pacman -U maya-substance-2.1.9-1-x86_64.pkg.tar.zst`

### 4. It's done.
