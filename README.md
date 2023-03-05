# hannah-montana-linux

Community project to upgrade Hannah Montana Linux to the latest version.

Current progress (please update!)

- follow ubuntu EOLUpgrades instructions https://help.ubuntu.com/community/EOLUpgrades
- remove medibuntu from apt sources and use sed to change mirrors list to contain "old-releases.ubuntu.com" for apt to run properly. 
- Dist-upgrade gives a "no attribute" issue, caused by trying to make a jump that was too big. 
- instead manually jumped just one updatee on the list https://changelogs.ubuntu.com/meta-release
- Upgrading to Karmic seems to kill the Hannah Montana background :( 
- Getting lots of "cannot open pixbuf loader module file" errors, so the issue seemed to be this: https://bugs.launchpad.net/ubuntu/+source/gdk-pixbuf/+bug/619003, reinstalling gdk-pixbuf2.0-0 fixed it.
- big issues with "no candidate for" which was fixed here https://butwt.wordpress.com/2020/06/29/problems-upgrading-ubuntu-server-lts/
	- but then we had issues which were fixed here https://ubuntuforums.org/archive/index.php/t-1749119.html
  - but then the networking stack and gui arent working and I have to switch to TTY2 to get anything.
