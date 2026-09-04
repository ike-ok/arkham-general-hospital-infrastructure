# Group Policy — Automated Drive Mapping

The Clinical share `\\FILE01\\Clinical` is mapped to drive `L:` using Group Policy Preferences. Item-level targeting restricts the mapping to `GG_Clinical`. The GPO is linked to the Clinical Services OU and was validated with `gpresult /r` and client testing.
