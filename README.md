<div align="center">
  <img width="500" height="350" src="assets/img/logo.svg" alt="Awesome">
</div>

# Awesome Tools [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) <!-- omit in toc -->

An awesome list of useful tools, OSes, utilities, and software packages.

## Contents <!-- omit in toc -->

- [Windows](#windows)
- [Linux](#linux)
  - [Linux OSes](#linux-oses)
    - [Debian Family](#debian-family)
    - [RedHat Family](#redhat-family)
    - [Other Linux](#other-linux)
- [Cross Platform](#cross-platform)
- [Programming](#programming)
  - [Python](#python)
    - [Package Managers](#package-managers)
    - [Python Packages](#python-packages)
      - [Azure](#azure)
      - [Configuration](#configuration)
      - [Dev Tools](#dev-tools)
      - [Database/ORM](#databaseorm)
      - [Data Packages](#data-packages)
      - [HTTP utilities](#http-utilities)

## Windows

Tools for the Microsoft Windows OS.

- [PowerToys](https://learn.microsoft.com/en-us/windows/powertoys/) - Official package from Microsoft to add extra "power user" functionality, like caffeinate (keep your computer awake & unlocked for a configurable length of time), extract text from screenshots, color picker, monitor zones, & more.
- [ShareX](https://getsharex.com) - Free, OSS screenshot tool. More capable than Windows' built-in screenshot utility, and can upload to multiple different storages like Dropbox, Onedrive, or Google Drive.
- [Windows Terminal](https://github.com/microsoft/terminal) - A more modern terminal experience for Windows. Can switch your active session between PowerShell, CMD, and any other prompts installed like the Azure CLI or Git bash CLI.
- [Winget CLI](https://github.com/microsoft/winget-cli) - Finally...Windows has caught up to the early '90's and has an official package manager. 
- [Windows Sandbox](https://learn.microsoft.com/en-us/windows/security/application-security/application-isolation/windows-sandbox/windows-sandbox-overview) - Official, built-in sandbox utility (must be enabled). Explode suspicious binaries in an isolated environment, or isolate sensitive software from the rest of the OS. Configurable using [XML](https://learn.microsoft.com/en-us/windows/security/application-security/application-isolation/windows-sandbox/windows-sandbox-configure-using-wsb-file).
- [BCUninstaller](https://www.bcuninstaller.com) - The "Bulk Crap Uninstaller" is an open source utility for removing large amounts of unwanted applications quickly. The app presents the user with a list of installed applications that can be multi-selected using checkboxes. BCUninstaller then loops over every checked app and runs its uninstaller. Most apps can be uninstalled "unattended," the BCUninstaller utility will automate uninstallation steps when available, so you can start the uninstaller and leave the machine for a few minutes. At the end, the app will offer to backup & clean the registry to remove remnants of the uninstalled apps, and will search the filesystem for leftover files & links for each uninstalled app.
- [WizTree](https://www.diskanalyzer.com/) - "The fastest disk space analyzer." Like [WinDirStat](https://windirstat.net/), this tool scans a target disk (i.e. `C:` or `D:`) and presents you with a size-ordered list of files & directories, helping you to quickly spot large files & folders taking up space on your hard drive. The tool makes cleaning up your disk to free up storage space much easier than manually clicking through the file explorer. The main advantage of WizTree over WinDirStat is speed, WizTree is *many* times faster to scan large amounts of data.
- [PeaZip](https://peazip.github.io/) - While Windows is getting better at built-in archive support, there are still a number of formats (like `.tar.gz`) that Windows cannot handle natively. PeaZip is my go-to archiving utility, it supports a [very large range of archive formtas](https://peazip.github.io/peazip-free-archiver.html), it's free and open-source, and it integrates well with the Windows context menu (right click).
- [Devolutions Remote Desktop Manager](https://devolutions.net/remote-desktop-manager/) - Free (with an optional paid edition that has features a team might use) RDP connection manager for Windows. You can organize your sessions into folders, and while it is geared at RDP, this tool supports a ton of connection types (`ssh`, `(s)ftp`), TeamViewer, Apple Remote Desktop, Azure/Amazon S3 storage, and many other types of connections. Also has an option of storing connections in an encrypted SQLite database, making importing/exporting sessions easy!
- [Remote Desktop Connection Manager (RDCMan)](https://learn.microsoft.com/en-us/sysinternals/downloads/rdcman) - An official Microsoft tools for RDP sessions. Save your connections to a list, open multiple RDP connections from the same interface, script sessions, etc.
- [Ventoy](https://ventoy.net/en/index.html) - A utility for creating bootable USB drives. Use the installer to create a Ventoy media, then you can simply drop `.iso` files on the drive. When you boot from the disk, Ventoy will automatically find all bootable ISOs and present them in a menu for you to boot from. For UEFI/secure-boot enabled devices, Ventoy provides a certificate you can install from the USB (created at the same time you install Ventoy on the drive, automatically) to enable booting from Ventoy without disabling/fiddling with secure boot.

## Linux

Where to start...where to end! The list of usefulness I've found for Linux OSes deserves its own awesome list! This is an incomplete list of some of my favorite tooling for Linux.

### Linux OSes

[Linux is just a kernel](https://itsfoss.com/linux-kernel-os/). In practice, anyone you talk to will know what you mean if you say you "run Linux," but if you're a pedant like the once-great Richard Stallman, you may prefer to refer to Linux operating systems as "distributions." You will also hear them referred to as "flavors."

Here are some of the best distributions, sorted by their family tree (Debian, RedHat, or "other"/independent).

---

#### Debian Family

Debian, the root ancestor for all distributions that use the `.deb` packaging format, is a rock-solid, stable, familiar OS that "runs on anything." The Debian OS is incredibly stable, and runs on a wide variety of hardware. Debian serves as the base image for a number of popular Linux distributions/"flavors," including Ubuntu, Kali Linux, the Raspberry Pi OS, and more.

- [Debian](https://www.debian.org) - One of the most influential OSS projects in the world, Debian is not the most up-to-date, "bleeding edge" OS, and that is by design. The stability & predictability Debian provides is the trade off for a package library that is at times behind on major releases.
- [Ubuntu](https://ubuntu.com) - A very popular, established Linux distribution that is beginner and enterprise friendly, is backed by a corporation (ensuring its longevity). The Ubuntu OS is "opinionated," there are a number of defaults, configurations, and packages (like `snapd`) that are defaults in Ubuntu and may not be everyones' preference.
- [Linux Mint](https://www.linuxmint.com/) - Based on Ubuntu. A commonly recommended distribution for Linux newbies coming from Windows, Linux Mint is a stable, friendly distribution that offers a number of conveniences like driver/firmware management. Its main selling point is that "everything just works 'Out of the Box'."
- [Proxmox](https://www.proxmox.com/en/proxmox-virtual-environment/overview) - A hypervisor alternative to VMWare ESXi, Microsoft Hyper-V, etc. Can manage traditional VMs as well as LXC containers.
- [Pop_OS!](https://pop.system76.com/) - Based on Ubuntu. A fast, secure OS by System76, Pop_OS! is one of the more exciting Linux distributions. Users who enjoy Ubuntu on the desktop but do not want to deal with Ubuntu's defaults or the `snap` package manager can install Pop_OS! for a machine that is compatible with all Ubuntu packages & guides. Pop_OS! develops its own desktop environment, Cosmic, which feels familiar to the GNOME desktop environment, but is more modern and configurable.
- [Rescatux](https://www.supergrubdisk.org/rescatux/) - A Debian-based live distribution for rescuing broken Linux and Windows bootloaders. Its gloriously shitty, dated interface belies one of the most useful boot rescue toolsets I've encountered. This image has saved countless installs for me, ranging from server hardware, laptops, to VMs. No live USB is complete without this image.
- [Kali Linux](https://www.kali.org) - The defacto penetration testing distribution. Kali Linux is a continuation of the [Backtrack Linux](https://www.backtrack-linux.org) project (discontinued in 2013), and is arguably the most popular security-oriented Linux distributions available. Installable on a wide range of hardware, including [Android phones](https://www.kali.org/docs/nethunter/), Kali is a portable, powerful, and approachable tool for learning Linux, penetration testing, cybersecurity, and computer forensics. There is a large community of users with many great YouTube videos, guides/how-tos, and other forms of community support.
- [Parrot OS](https://www.parrotsec.org) - An alternative/competitor to Kali Linux, this distribution focuses on being a versatile pentesting and computer forensics OS. Parrot can be booted from a USB stick as a live image, or installed to a disk and used as a persistent OS. It is aimed at providing a suite of pentesting and security tools that are more discoverable & easier to use than Kali, Parrot tends to prefer GUI versions of popular tools like NMAP (the CLI versions are also available/installed).

---

#### RedHat Family

RedHat is an enterprise-grade Linux distribution that, similarly to Debian Linux, serves as the base for a number of popular downstream Linux distributions. RedHat uses the `.rpm` packaging system, distinguishing itself from the `.deb` ecosystem. Backed by the IBM corporation after a [buyout](https://www.redhat.com/en/ibm) of the RedHat Corporation [in 2019](https://www.redhat.com/en/about/press-releases/ibm-closes-landmark-acquisition-red-hat-34-billion-defines-open-hybrid-cloud-future), RedHat is one of the oldest Linux distributions. Its aim is to be a stable, secure by default OS for enterprise users, while keeping a more up-to-date list of packages compared to Debian.

Although RedHat itself requires an enterprise license, the project provides a downstream community edition with the Fedora OS distribution which you can use to familiarize with the RedHat ecosystem.

- [RedHat Enterprise Linux](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux) - The base image for a number of downstream `.rpm` distributions. One of, if not *the*, most profitable open-source company in the world, RedHat is aimed at enterprise customers, but provides downstream releases for the community with Fedora.
- [Fedora](https://fedoraproject.org/) - Officially maintained by the RedHat enterprise, Fedora is compatible with the `.rpm` packaging system, and is meant as a "bleeding edge" testbed for RedHat Enterprise Linux. Fedora gets package and OS updates before RedHat, and the community tests and refines these releases by using Fedora as their OS, improving each release of RedHat.
- [Alma Linux](https://almalinux.org/) - With the [death of CentOS](https://www.redhat.com/en/blog/centos-linux-going-end-life-what-does-mean-me), a number of distributions have popped up to fill the "binary-compatible with RedHat, enterprise grade, consumer edition" of RedHat Enterprise Linux.
- [Rocky Linux](https://rockylinux.org) - Another successor to CentOS, Rocky Linux was started by one of the original founders of CentOS in response to its discontinuation in 2019.

---

#### Other Linux

Independent Linux distributions that use their own package management system. These are not descendents of either Debian or RedHat, but use the same Linux kernel.

- [Arch Linux](https://archlinux.org/) - I use Arch, btw. Arch linux is an independent distribution notorious for its incredibly useful & well-maintained [Arch Wiki](https://wiki.archlinux.org/). Arch is a "rolling release" distribution, meaning you do not have to reboot after most system updates. Many experienced Linux users recommend going through the [Arch OS installation](https://wiki.archlinux.org/title/Installation_guide) to gain a better understanding of the internals of a Linux OS. The idea behind Arch Linux is that you get "just enough OS" to boot your machine, with a very minimal OS install that you build up from by installing only the packages you need.
  - [EndeavorOS](https://endeavouros.com) - With the [death of AntergOS Linux in 2019](https://www.phoronix.com/news/Antergos-EOL), a number of Arch downstream Linux distributions popped up to fill the gap. EndeavorOS is one of the closest spiritual successors to AnetergOS. The goal of Endeavor is to give users access to the Arch OS package library, while configuring sane defaults and packages to make the experience more "beginner friendly."
  - [Manjaro Linux](https://manjaro.org) - Manjaro, like EndeavorOS, provides an OS based on Arch Linux and compatible with Arch's package repository, while offering some default packages & configurations (as well as a graphical installer) to ease users into the Arch ecosystem.
- [Alpine Linux](https://www.alpinelinux.org/) - Alpine Linux is a small and secure OS with its own package repositories and package management tool (`apk`). The image is commonly used as the base image for Docker containers.
- [NixOS](https://nixos.org/) - A "declarative/immutable OS," where the OS is configured using a series of text files to describe a desired running state for your machine. This can include configurations like network interfaces, hostnames, base packages, etc. The idea behind Nix is that you can back your OS state up to version control like Git, and have a reproducible build so each time you install your OS, it matches your configuration 1-to-1. Configurations can be updated over time, and updates to the OS or packages use a "swapping" system so you do not need to reboot your machine to apply updates.

## Cross Platform

Tools and utilities installable on more than 1 major OS.

- [VLC](https://www.videolan.org/vlc/) - One of the best OSS projects on the Internet. VLC can open nearly any media file you will encounter, and has tools for converting between formats and encodings. The maintainer of VLC has [turned down millions of dollars](https://news.ycombinator.com/item?id=15372048) to implement ads and tracking into VLC, making this software trustworthy and hinting at strong leadership and adherence to the principles of open source software.
- [MPV](https://mpv.io/) - A versatile, cross-platform media player. Similar in spirit to VLC Media Player, MPV is well received by the community and even preferred over VLC by some.
- [FFMPEG](https://ffmpeg.org) - The "swiss army knife" of media file conversion. Although this is a different tool from VLC, it performs a similar function, albeit from the CLI rather than with a GUI. The `ffmpeg` binary is cross-platform and emeddable, you can call it from the CLI or scripts, and the syntax is nice and easy! For example, to convert a `.mp4` to a `.avi`: `$> ffmpeg -i input.mp4 output.avi`

## Programming

I'm not much of a programmer, but I do enjoy tinkering with languages, specifically Python, Bash, and PowerShell. This section covers some useful packages and tooling I use regularly, or I think are worth mentioning as an "awesome" addition to your stack.

### Python

[Python](https://www.python.org) is a flexible and powerful programming language well suited to a great many tasks. The language is "interpreted" (versus a compiled language where your code is compiled into a distributable binary, i.e. a Linux binary or Windows `.exe`). When you run Python code, your code is "translated" from source code directly to bytecode, and your shell executes that bytecode. This leads to some compilation overhead, and you may notice a delay between running your script with the `python` command and the program actually executing. Once the code is transpiled, the program will execute as fast as Python's [Global Interpreter Lock (GIL)](https://realpython.com/python-gil/) will allow.

Below are some packages and tooling I use/have used that are worth sharing.

#### Package Managers

Python's default/built-in package manager, [pip](https://docs.python.org/3/installing/index.html), is a capable project manager with some shortcomings. These project managers approach Python project management from a more "modern" experience. Some of these package managers take inspiration from Rust's elegent [cargo](https://doc.rust-lang.org/cargo/) package manager.

- [PDM](https://pdm-project.org) - A project management tool for Python. Handles project initialization & scaffolding, `.venv` creation, package management, building & publishing, and project scripts. Uses the [pyproject.toml](https://packaging.python.org/en/latest/guides/writing-pyproject-toml/).
- [uv](https://docs.astral.sh/uv/) - A ridiculously fast Python project manager written in Rust. Handles `.venv` creation, package management (with an incredibly fast resolver & a superpowered cache), and project scripts.
- [pixi](https://pixi.sh/latest/) - An exciting new Python project manager that uses Conda channels for packages, and more recently pypi packages. Handles interpreter installation (Python, Rust, and R), project initialization & management, package management, project scripts, & more.
- [Conda](https://docs.conda.io/en/latest/) - The package manager for data scientists. Good for installing large ML libraries like `pytorch`.
- [Mamba](https://mamba.readthedocs.io/en/latest/) - A fully compatible replacement for Conda that is much, much faster at resolving dependencies.
- [Micromamba](https://mamba.readthedocs.io/en/latest/user_guide/micromamba.html) - A small, statically linked binary that supports a subset of all `mamba` or `conda` commands, and is much, much faster than either.

---

#### Python Packages

Python packages can be installed from a number of sources, the default being the official [Pypi](https://pypi.org) (Python Packaging Index). The [package managers](#package-managers) in the section above aid with installing dependencies, some of them use the Conda channels instead of Pypi.

##### Azure

Microsoft provides first-class support for interacting with Azure in Python by way of the [Azure SDK for Python](https://learn.microsoft.com/en-us/azure/developer/python/sdk/azure-sdk-overview). You generally only need to install the `azure-core` library, but there are links to documentation for individual modules in the core package below.

- [Azure Core](https://pypi.org/project/azure-core/) - Provides an SDK for interacting with Microsoft Azure.
- [Azure Blob Storage](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-python?tabs=managed-identity%2Croles-azure-portal%2Csign-in-azure-cli&pivots=blob-storage-quickstart-scratch) - Library for interacting with Azure Blob Storage.

---

##### Configuration

Stop hardcoding your secrets into your script! Configuration management is a widely debated topic with many competing philosophies on "best practice." Decoupling your configuration from your code, like with the [12-factor app](https://12factor.net) philosophy, provides a layer of security while also adding flexibility to your program. It is much easier to change a variable in your environment or a local file than it is to hunt for it throughout your code.

- [Dynaconf](https://www.dynaconf.com) - A configuration management library that follows the [12-factor app](https://12factor.net) development principle. The main concept is to separate your configuration from application logic. Loads environment variables dynamically from your environment, `.toml` file(s), `.json` file(s), `.env` file(s), and more.

---

##### Dev Tools

Tools to make developing Python packages easier/more robust.

- [Ruff](https://docs.astral.sh/ruff/) - A fast, versatile code linting & checking tool. Combines functionality of tools like `Flake8`, `black`, `isort`, & more. Uses a `[tool.ruff]` section in your `pyproject.toml` or a `ruff.toml` to define rules.
- [Nox](https://nox.thea.codes/en/stable/) - A cross-platform CLI tool that automates testing & more. An alternative to the [tox]() library, written entirely in Python. This allows for much more flexibility.
- [pytest-xdist](https://pytest-xdist.readthedocs.io/en/stable/) - Extends the [pytest](https://docs.pytest.org/en/stable/) testing frametwork to allow for running multiple tests simultaneously.

---

##### Database/ORM

Python has many libraries for interacting with databases. SQLAlchemy is one of the most popular, and arguably the most worth learning. Many ORMs and database connectors offer similar functionality, but there are tradeoffs with nearly all of them. SQLAlchemy is possibly the most "feature complete" ORM for Python, and in fact can act as a direct database driver if needed.

This section will grow over time.

- [SQLAlchemy](https://docs.sqlalchemy.org/en/latest/index.html) - One of (if not *the*) most flexible, powerful ORMs for Python. There is a learning curve with SQLAlchemy, but the new [ORM syntax](https://docs.sqlalchemy.org/en/20/orm/quickstart.html) in SQLAlchemy v2.0 makes the code more "Pythonic."

---

##### Data Packages

- [Pandas](https://pandas.pydata.org) - The defacto Python dataframe library. Load datasets from Python `dict`s, `.parquet`/`.csv`/`.json` files, a database backend (using SQLAlchemy) or create on the fly. The dataframe is stored in memory and can act as an in-memory alternative to a database table.
- [Polars](https://pola.rs) - A newer Python dataframe library, written in Rust. Some compatibility issues on certain platforms (like ARM64), which can be worked around. ~30x faster than other dataframe libraries, and a more "Pythonic" API.
- [Ibis](https://ibis-project.org) - A dataframe library that "works with any data system." Ibis uses [DuckDB](https://duckdb.org) for its backend, and can connect to multiple database backends, and work with multiple dataframe backends. This allows for developing data analysis/processing functions once, and swapping your database & dataframe backends without affecting the underlying functionality.
- [DuckDB](https://duckdb.org/docs/api/python/overview.html) - An in-process database management system. Can load extremely large datasets to an in-memory database. Useful for loading a subset of data from a large database for local processing/analysis, instead of querying the database each time, you query it once, load the data into DuckDB, and then operate on your "local" copy. Can handle writing modifications back to the original database.
- [Jupyter](https://jupyter.org) - Interactive notebooks that let you write code in "cells" which you execute manually. Great for data projects, prototyping, data processing, and more.
  > Note: If you are using a `.venv`, you must install the `ipykernel` package in the virtualenv for it to be detected as a useable kernel.

---

##### HTTP utilities

The [requests](https://docs.python-requests.org/en/latest/index.html) module is the defacto package for making HTTP requests an doing something with the response. There's nothing wrong with `requests`, but it is not an asynchronous library. The utilities below are alternatives to `requests` you can try if the `requests` packages do not cover your needs.

- [HTTPX](https://www.python-httpx.org) - A fully-featured, fast, flexible HTTP client for Python that offers synchronous and asynchronous APIs, supports HTTP/1.1 and HTTP/2, and will feel familiar to `requests`. `httpx` is more configurable than `requests`, and can use plugins like `hishel` for caching.
- [Hishel](https://hishel.com) - A caching library for HTTPX. Offers a highly configurable API for adding in-memory, file-based, and database-backed caches for HTTP responses made with the HTTPX library.
