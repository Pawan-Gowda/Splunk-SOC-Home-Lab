# SPL Queries Used in This Lab

## Detect All Failed Login Attempts
source="/var/log/auth.log" "Failed password"

## Count Failed Logins by Host
source="/var/log/auth.log" "Failed password" | stats count by host

## Timeline of Failed Login Attempts
source="/var/log/auth.log" "Failed password" | timechart count

## Alert Condition
Triggers when failed login attempts exceed 3 in a one hour window
