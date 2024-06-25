# Shiro 1 Extractor

This repository contains a Python script `shiro1-extractor.py` that will search all `.pcl` files within a specific directory and extract Apache Shiro 1 hashes from them, then write them to an output file.

## Usage

```
usage: shiro1-extractor.py [-h] input_dir output_file

Extract Apache Shiro 1 hashes from .pcl files for use with Hashcat.

positional arguments:
  input_dir    Directory path containing the .pcl files
  output_file  Output file to save the hashes

options:
  -h, --help   show this help message and exit
```

## Hashcat Module

I have developed a custom Apache Shiro 1 hashcat module while the official project is still lacking support for the algorithm. It is available at my hashcat fork [here](https://github.com/fin3ss3g0d/hashcat). You can take the hashes extracted using this program and use them directly with the module. Here are the steps to use it:

1. Clone the [repository](https://github.com/fin3ss3g0d/hashcat)
2. Build it from source
3. Module is accessible using mode `12150`

I have submitted a [pull request](https://github.com/hashcat/hashcat/pull/4017) to the official Hashcat project, hopefully it will get merged and the module will be available via the official Hashcat repository! A blog was created for the creation of the Hashcat module and is available [here](https://fin3ss3g0d.net/index.php/2024/06/24/crack-faster-hack-smarter-custom-hashcat-module-for-apache-shiro-1-sha-512/).

## CVE-2024-4956

A script to automate exploiting `CVE-2024-4956`, a path traversal vulnerability in Sonatype Repository 3 allowing unauthenticated attackers to read system files is available [here](https://github.com/fin3ss3g0d/CVE-2024-4956). Sonatype Repository 3 uses the Apache Shiro 1 hashing algorithm at the time of writing and stores user hashes inside of OrientDB .pcl files. A sample of 155 known OrientDB .pcl existing file paths are included in the repository.

## Shiro1Tools

[This repository](https://github.com/fin3ss3g0d/Shiro1Tools) contains useful tools that were used when creating the Hashcat module for Apache Shiro 1 such as a standalone `C` program that cracks Apache Shiro 1 hashes using OpenSSL and a `Java` application for generating Apache Shiro 1 hashes.

## Disclaimer

This program is intended for legitimate and authorized purposes only. The author holds no responsibility or liability for misuse of this project.