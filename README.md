This is a simple utility using Ansible for syncing ssh keys onto a set of servers. e.g., if you have per-device keys (which is what I'm using it for), or if you want to grant people access to multiple servers at once. It's currently built to work with per-host usernames, for those of us who end up with SSH access to a mixed set of servers where the default sudo-capable user is under a different name. 

To use, place a `valid_keys` subdirectory into your inventory directory, and place individual `*.pub` public key files in there. Ditto with `revoked_keys` (for decomissioned devices, or team members who leave, etc.).

`-e "host_pattern=$SOME_PATTERN"` can be used to select a specific group of hosts.
