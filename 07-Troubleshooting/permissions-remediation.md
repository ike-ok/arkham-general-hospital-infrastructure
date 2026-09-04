# Troubleshooting — Research Permissions

A Research-share permissions issue was investigated where generic `BUILTIN\\Users` access was broader than intended. Generic user access was removed while preserving `DL_Research_RW`, `DL_Research_RO`, `SYSTEM`, and `Administrators`. Authorized and unauthorized access were then tested.
