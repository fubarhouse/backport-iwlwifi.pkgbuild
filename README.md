# PKGBUILD for Ubuntu iwlwifi backport

## Summary

Ubuntu supports iwlwifi on the latest Linux kernel, opposed to official sources which have a limited support cycle.

iwlwifi isn't compiled against the latest kernel - and I need the supported version to use wifi on my work laptop.

So, this repository exists as a repeatable way for me to keep my wifi drivers up to date with a level of automation.

## Caution

This `PKGBUILD` breaks a number of conventions - and installs the modules directly to the system as part of the build process.

It's a quick and dirty way of running a repeatable sequence of events, so it should be used with some caution.

## License

MIT - I provide no warranty or guarentee. Use at your own risk.