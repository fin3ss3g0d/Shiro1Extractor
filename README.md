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

Blog post covering all of this coming soon!