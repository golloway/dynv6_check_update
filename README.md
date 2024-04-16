# dynv6_check_update

A reliable and practical shell script designed to efficiently detect and update DDNS records with dynv6.

This shell script offers a practical solution for detecting and updating DDNS records with dynv6. It retrieves both IPv4 and IPv6 addresses from the ppp0 interface and checks if the current DDNS records have been updated on dynv6. If not, it submits the new IP addresses.

These operations are transferable to other DDNS service providers as well. The critical component is to utilize a nameserver provided by the service provider to ensure reliable submission results.

The script can be scheduled for automatic execution using crontab:


*/2 * * * * /path_of_script/check_update_ddns.sh > /dev/null
