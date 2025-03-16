# Forced Authentication

A Forced Authentication attack involves attackers exploiting automatic authentication mechanisms in protocols like SMB (Server Message Block) and WebDAV (Web Distributed Authoring and Versioning) to intercept credential information, such as account hashes.

https://attack.mitre.org/techniques/T1187/

## Overview
This script automates the process of interacting with SMB shares. It takes a list of SMB share paths from a file and executes commands on them, such as uploading specific files. 

## Features
- Connect to multiple SMB shares using credentials provided by the user.
- Perform specific commands (`put @test.scf`, `put @test.url`, `put @test.library-ms`) on each SMB share.

## Prerequisites
- Bash should be installed and operational on your machine.
- `smbclient` must be installed on your system.
- Replace the placeholder ATTACKER_IP with the IP address of your listener in the files: @test.library-ms, @test.scf, and @test.url.

## Usage
To execute the script, use the following command format:
```
./forced_authentication.sh 'FQDN/USERNAME' 'PASSWORD' FILENAME
```

To clean up, use the command:
```
./clean_up.sh 'FQDN/USERNAME' 'PASSWORD' FILENAME
```
