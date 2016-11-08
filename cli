#!/bin/sh

sys=`uname`

if [ $sys = "Darwin" ]
then
	url=`curl -s https://api.github.com/repos/appfront/cli/releases | grep browser_download_url | head -n 1 | cut -d '"' -f 4`
	echo "installing..."
	curl -sS $url > appfront
	chmod +x ./appfront
else
	url=`wget -qO- https://api.github.com/repos/appfront/cli/releases | grep browser_download_url | head -n 1 | cut -d '"' -f 4`
	echo "installing..."
	wget -qO- $url"_linux" > /usr/local/bin/appfront
	chmod +x /usr/local/bin/appfront
fi

echo "the Appfront CLI is now installed, please type appfront -help"
