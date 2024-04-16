# Reliable and Practical DDNS Update Shell Script

## Overview
This shell script is designed to efficiently detect and update dynamic DNS (DDNS) records with dynv6. It offers a robust solution for managing DDNS updates, ensuring your network configurations are always current.

## Features
- **IP Address Retrieval**: Automatically retrieves both IPv4 and IPv6 addresses from the `ppp0` interface.
- **DDNS Record Verification**: Checks if the current DDNS records have been updated on dynv6.
- **IP Address Submission**: Submits new IP addresses if the existing records are outdated.

## Compatibility
The operations can be adapted for use with other DDNS service providers. The key to success is using a nameserver provided by your service provider, ensuring that submissions are reliable.

## Automation
Schedule the script for automatic execution with `crontab` to keep your DDNS records consistently updated without manual intervention.

```bash
*/2 * * * * /path_of_script/check_update_ddns.sh > /dev/null
```
