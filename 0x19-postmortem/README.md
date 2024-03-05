WWW.ALXBNB.TECH OUTAGE INCIDENT REPORT
Issue Summary
From March 4th 2.00PM EAT to 2.15PM EAT, requests made to alxbnb.tech resulted in 403  forbidden error, affecting all users attempting to access the site during the outage. Approximately 100% of users were affected. This was caused by misconfigurations in the Nginx configuration files.
Timeline(All Times are East African Time)
2.00PM - Automatic puppet system configuration is done.
2.05PM - Outage begins(access denied with 403 forbidden)
2.06PM - Monitoring system alerts operations team
2.08PM -Initially explored network connectivity issues and potential DDoS attacks, which proved to be irrelevant.
2.10PM - Checking of Config files and finding the cause is due to recent configuration
2.12 PM - Identified misconfigurations in the Nginx configuration files, specifically related to automatic puppet system configurations.
2.15PM - Restored the previous version of the Nginx configuration files to resolve the 403 Forbidden error.

Root Cause and Resolution
The issue stemmed from misconfigurations in the Nginx configuration files, introduced during an automatic puppet system configuration.At 2.06PM EAT monitoring systems notified the operations team who investigated and found the automated update was done on all the wrong config files. The team then started the roll back and reverted the Nginx configuration files to the previous version, eliminating the misconfigurations causing the 403 Forbidden error.

Corrective and Preventative Measures
Disable the current automatic configuration files.
Correct the puppet files to the intended configuration files
Improve the monitoring system to be more alert
Implement stricter change management processes to prevent unintended configuration changes.

Tasks
Develop automated tests for Nginx configuration files to catch errors before deployment.
Review and update puppet configuration scripts to ensure they do not introduce unintended changes.
Conduct regular audits of system configurations to identify and rectify any discrepancies.
Enhance documentation outlining proper Nginx configuration practices to avoid future misconfigurations.

