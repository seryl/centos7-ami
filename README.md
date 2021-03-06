# CentOS 7 AMI

This is the shell script used to build the Bashton CentOS 7 AMIs we have
made publicly available.  To use, start a RHEL7 or CentOS 7 instance,
attach a blank EBS volume at /dev/xvdb and the script will do the rest.

If you just want to run the images, or modify using
[Packer](http://packer.io/), you can find AMI ids at
http://www.bashton.com/blog/2015/centos-7-2-1511-ami/

## Differences from official CentOS marketplace AMI

- Uses gpt partitioning - supports root volumes over 2TB
- Includes [out of tree ixgbevf
  driver](http://sourceforge.net/projects/e1000/files/ixgbevf%20stable/3.0.2/)
  providing [enhanced
networking](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/enhanced-networking.html)
  only instance types that support it
- Local ephemeral storage mounted at `/media/ephemeral0`
- Default user account `ec2-user`

