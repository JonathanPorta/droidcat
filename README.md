# DroidCat: Android Data Extraction and Backup Unpacking Tool

DroidCat is a fledgling, yet versatile command-line utility designed for extracting data from Android devices and unpacking Android backup files (.ab). This tool simplifies the process of pulling accessible data and app data from a connected Android device and offers functionality to unpack and decrypt Android backup files.

## Features

- **Data Extraction**: Efficiently pull data and app data from connected Android devices.
- **Backup Unpacking**: Unpack and decrypt password-protected `.ab` backup files into a readable format.
- **Custom ID Tagging**: Option to tag extraction and backup operations with a custom identifier for easy organization.
- **Helpful Documentation**: Includes usage instructions to guide through each available command.

## Prerequisites

Before using DroidCat, ensure the following requirements are met:

- **ADB (Android Debug Bridge)**: Must be installed and properly configured on your system. Verify its installation by running `adb version` in your terminal.
- **Java**: Required for running the Android Backup Extractor (ABE). Ensure Java is installed and available in your system's PATH.
- **Android Backup Extractor (ABE)**: DroidCat relies on ABE for unpacking .ab files. ABE must be present in the system's PATH. ABE can be obtained from [https://github.com/nelenkov/android-backup-extractor](https://github.com/nelenkov/android-backup-extractor). Follow the installation instructions provided in the repository to ensure ABE is set up correctly.

## Installation

1. Clone or download the DroidCat script to your local machine.
2. Ensure that `adb`, `java`, and `abe.jar` are in your system's PATH, or adjust the script to point to their locations.
3. Make the script executable by running `chmod +x droidcat` in your terminal.

## Usage

DroidCat can be invoked with the following commands:

### Extract Data from Device

```sh
./droidcat extract [ID]
```

This command pulls all accessible data from the connected device. If an optional ID is provided, it tags the backup directory and file names for easy identification.

### Unpack an Android Backup File

```sh
./droidcat unpack /path/to/backup.ab [password]
```

Unpacks a given Android backup file. If the backup is password-protected, provide the password as the second argument. If no password is provided, the script attempts to unpack the backup without a password.

### Display Help Information

```sh
./droidcat --help
```

Shows usage information for DroidCat, detailing available commands and options.

## Note on ABE

The Android Backup Extractor (ABE) is essential for unpacking .ab files. Ensure that `abe.jar` is located in a directory included in your system's PATH or adjust the `unpack_backup` function in the DroidCat script to point directly to its location.

## Contributing

Contributions to DroidCat are welcome! Please refer to the project's issues and pull requests to propose improvements or submit bug fixes.

## License

DroidCat is distributed under the MIT License. See the LICENSE file for more information.

---

DroidCat is designed to simplify data extraction and backup management for Android devices, streamlining what can otherwise be a complex process. Whether for backup, recovery, or analysis purposes, DroidCat offers a powerful toolset for Android data handling.
