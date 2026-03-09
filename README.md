# Supabase Keep‑Alive

This repository contains:
- A GitHub Actions workflow that periodically pings my Supabase projects to prevent them from being paused on the free tier.
- A GitHub Pages dashboard showing the last ping time and uptime for each project.

## Projects
- Track2Link


## How it works
The workflow calls the `ping_keep_alive` RPC function in each Supabase project, which updates a `keep_alive` table (incrementing `uptime_days` and setting `last_ping` to now). The dashboard fetches this data using the public anon key.