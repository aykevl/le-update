Let's Encrypt automatic updater

Run this program every day to let it check for expired certificates.

It checks `/etc/nginx/sites-enabled` for site names, and assumes the webroots
have the same name in `/srv` (e.g. `/srv/example.com`). All names on the same
domain directly on a TLD are taken together in a SAN certificate. E.g.
example.com, www.example.com and mail.example.com are taken together. No
checking is done via publicsuffix for public suffixes that are more than one
part long (TODO).

This is not a finished script. It is not properly tested and may miss some
things. But it works for me.
