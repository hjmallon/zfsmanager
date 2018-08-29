# ZFS Manager

ZFS administration tool for [Webmin](http://www.webmin.com/).

This is in early development, not for production. That being said, try this out in a virtual machine or anywhere else where data is non-critical. My hope is that this will ultimately provide Webmin with similar ZFS functionality to FreeNAS and NAS4Free.

This project lives at [GitHub](https://github.com/jonmatifa/zfsmanager), please provide all feedback and bug reports there. I am brand new to Perl and Webmin's API, so first I apologize for the shabby state the code is in, second any further contributions are greatly welcomed. I am learning a fair amount about ZFS along the way as well.

I am currently developing this under ZFS on Linux in Ubuntu, but all varients of ZFS/Webmin are planned to be supported in the future.

## Installation

You will need `perl-Data-Dumper` installed for everything to work. (e.g. on CentOS do "`yum install perl-Data-Dumper`").

### Packaged

You can download the latest release from the [Releases tab](https://github.com/jonmatifa/zfsmanager/releases) as a `zfsmanager-VERSION.wbm.gz` file.

Navigate to `Webmin Configuration` -> `Webmin Modules` and install using `From uploaded file`.

### From Git

You can get the latest code from git.

```sh
cd /usr/libexec/webmin # For RHEL/CentOS
# OR
cd /usr/share/webmin # For Debian/Ubuntu

# Get zfsmanager code
git clone https://github.com/jonmatifa/zfsmanager.git

# Copy default config
mkdir /etc/webmin/zfsmanager
cp zfsmanager/config /etc/webmin/zfsmanager

# Add zfsmanager to end of the lines with the desired users
vi /etc/webmin/webmin.acl

# That last part can also be done in the UI:
# - Navigate to Webmin Users -> USERNAME -> Available Webmin modules
# - Tick the box marked ZFS Manager
# - Press Save

# To keep up to date (in zfsmanager directory)
git pull
```

## Feedback

I am interested in what you think, even during this early alpha phase. The issue tracker can be used not only for bug reports but also feature requests and comments in general. Tracking and fixing bugs is important, but I also want to know what you think about the idea of the project and things like usability and UI design.

## Contribution

Right now its just me developing this. I'm not a programmer by trade, but I'm happy to work on this project whenever I can. I would love help from someone more seasoned at perl (don't judge me too hard), but also someone who "gets" the design philosophy of this project and understands the Webmin API. I'm a beginner myself so I'm not looking for too much.

## Thank you

Thank you for stopping by and I hope you enjoy this plugin!
