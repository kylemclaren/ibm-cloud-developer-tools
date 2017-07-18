# developer-tools-installer
These scripts performs an installation of the IBM Developer Tools CLI environment. The IDT is a plugin to the IBM Bluemix CLI. Our general target environment is the IBM Cloud, including public, dedicated, and local hybrid.

## Platforms

The following are platform specific concerns and notes you should be aware of.

### MacOS &amp; Linux Installation

The following command can install the IBM Developer tools in a single invocation.  Open up a terminal and run the following command:

```
$ curl -sL https://ibm.biz/idt-installer | bash
```

By default, this installer will use the 'brew' installer, if available. If you do not have `brew` available on your system, execute the following command with `--nobrew` option:

```
curl -sL https://ibm.biz/idt-installer | bash -s -- --nobrew
```

Access the [platform-specific readme](./linux-installer/README.md) for additional details.

This script has only been tested on Ubuntu Linux systems, although it should behave properly on other distros. If you run into any issues, please let us know on [Slack](https://ibm.biz/IBMCloudNativeSlack) or file an issue on our [GitHub repo](https://github.com/ibm-cloud-tools/idt-installer).



## Windows Installation
To install the IBM Developer Tools CLI on Windows 10 or newer:

1. Open Windows PowerShell by right-clicking and select "Run as Administrator".
2. Run this command:
```
Set-ExecutionPolicy Unrestricted; iex(New-Object Net.WebClient).DownloadString('http://ibm.biz/idt-win-installer')
```

Access the [Widnows-specific readme](./windows-installer/README.md) for additional details.

--- 

Once complete, there will be three aliases defined to access the IDT:
- `idt` : Main command line tool for IBM cloud native development (shortcut to 'bx dev')
- `idt-update` : Update your IDT environment to the latest versions
- `idt-uninstall` : Uninstall the IBM Developer Tools


## Feedback

We can be reached on [Slack](https://ibm.biz/IBMCloudNativeSlack) or file an issue on our [GitHub repo](https://github.com/ibm-cloud-tools/idt-installer).