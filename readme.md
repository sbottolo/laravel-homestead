<p align="center"><img src="https://laravel.com/assets/img/components/logo-homestead.svg"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/homestead"><img src="https://travis-ci.org/laravel/homestead.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/homestead"><img src="https://poser.pugx.org/laravel/homestead/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/homestead"><img src="https://poser.pugx.org/laravel/homestead/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/homestead"><img src="https://poser.pugx.org/laravel/homestead/license.svg" alt="License"></a>
</p>

## Introduction

Laravel Homestead is an official, pre-packaged Vagrant box that provides you a wonderful development environment without requiring you to install PHP, a web server, and any other server software on your local machine. No more worrying about messing up your operating system! Vagrant boxes are completely disposable. If something goes wrong, you can destroy and re-create the box in minutes!

Homestead runs on any Windows, Mac, or Linux system, and includes the Nginx web server, PHP 7.2, MySQL, Postgres, Redis, Memcached, Node, and all of the other goodies you need to develop amazing Laravel applications.

Official documentation [is located here](http://laravel.com/docs/homestead).


## Requirements for Windows
- VirtualBox 5.1.14
- Vagrant 1.9.1


## Solve performance issues

### Vagrant plugins

Official documentation for [Vagrant plugins installation](https://www.vagrantup.com/docs/plugins/usage.html)

Plugin list:
- vagrant-share    (1.1.9)
- vagrant-vbguest  (0.14.2)
- vagrant-winnfsd  (1.3.1)

```

vagrant plugin install vagrant-share
vagrant plugin install vagrant-vbguest
vagrant plugin install vagrant-winnfsd

```

### Homestead.yaml NFS config for Windows

```
[...]

folders:
    - map: ~/your/path
      to: /vagrant/path
      type: "nfs"
      owner: "vagrant"
      group: "vagrant"
      mount_options: ['nolock,vers=3,udp,noatime']
      
```
