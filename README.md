Here are some CLI commands and outputs that can help you identify the BIOS Version, serial number, model, username, and hostname of laptops and MacBooks.

Display a current BIOS version 
- **wmic bios get smbiosbiosversion**
    - Output: 
    `SMBIOSBIOSVersion`
    `1.27.0`

- **wmic bios get biosversion**
    - Output:
    `BIOSVersion`
    `{"DELL   - 2", "1.27.0", "Dell - 10000"}`

**systeminfo | findstr /c:"BIOS"**
    - Output:
    `BIOS Version: Dell Inc. 1.27.0, 17/03/2023`

**wmic bios get biosversion**
    - Output:
    `{"DELL   - 2", "1.27.0", "Dell - 10000"}`


Display a model name
- **wmic computersystem get model**
    - Output:
    `Model`
    `Latitude 5420`

- **wmic csproduct get name**
    - Output:
    `Name`
    `Latitude 5340`


## Display a username
**wmic computersystem get username**
    - Output:
    `UserName`
    `ID\yourlocalaccauntname`

- **whoami**
    - Output:
    `id\yourlocalaccauntname`

Display a hostname
- **hostname**
    - Output:
    `WR0A1B3CV4D5F`

- **wmic computersystem het name**
    - Output:
    `Name`
    `WR0A1B3CV4D5F`

- **wmic context | findstr /c:"NODE"**
    - Output:
    `NODE(S): WR6035E3fDCD`


## Display a serial number
- **wmic bios get serialnumber**
    - Output:
    `SerialNumber`
    `4ZW95M3`

- **wmic csproduct get IndentifyingNumber**
    - Output:
    `IdentifyingNumber`
    `4ZW95M3`

MAC **system_profiler SPHardwareDataType | grep "Serial"**
    - Output:
    `Serial Number (system): VIAKSLDFASD`

MAC **ioreg -l | grep "IOPlatformSerialNumber"**
    - Output:
    `"IOPlatformSerialNumber": VIAKSLDFASD`
