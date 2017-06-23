---
title: Making NHSbuntu
date: 2017-06-19
categories: Development
author_staff_member: 0rob-dyke
comments: true
---
NHSbuntu is built for the NHS from the Ubuntu open source operating system. To create our distribution we use tools from the Ubuntu ecosystem to package our customisations and build the download images. In this post I'll describe the techniques and tools we use for this.

## Customisations

Our core customisations are handled using a template from the ubuntu-default-settings package. This template allows us to easily set defaults for the look and feel of the desktop as well as tailoring the packages included in the installation.

Our customisations are as follows:
* NHSbuntu wallpaper!
* A look and feel similar to a well known desktop...
* NHSmail2 compatability
  * Email, calendar, address book
  * Messager, with file sharing!
* N3 VPN compatability
  * RSA token supported
* Remove games packages (sorry folks, no Minesweaper!)
* Added Remmina, a Remote Desktop client for VDI (or whatever it's called these days)

We have include our [own spinning logo at startup and shutdown](https://github.com/NHSbuntu/nhsbuntu-plymouth-gnome) and customised the [Ubiquity installation slideshow](https://github.com/NHSbuntu/nhsbuntu-default-settings/tree/master/ubiquity-slideshow).

Our customised settings packages are [published in our github repository](https://github.com/NHSbuntu/nhsbuntu-default-settings) and available as a [Launchpad PPA](https://launchpad.net/~nhsbuntu/+archive/ubuntu/ppa).

## Building

NHSbuntu is built on Ubuntu 16.04, the current LTS / Long Term Support release. We use live-build to create ISO files for you to use to install NHSbuntu. Our [live-build configuration](https://github.com/NHSbuntu/live-build-config) is published on github.

## Distributing

NHSbuntu installation ISOs can be [downloaded from our website](https://www.nhsbuntu.org/ISO/). We are also experimenting with [Artifactory](https://repo.nhsbuntu.org/) for releasing our [ISOs](https://repo.nhsbuntu.org/artifactory/list/nhsbuntu-iso/) and [Vagrant boxes](https://repo.nhsbuntu.org/artifactory/list/nhsbuntu-boxes/).
