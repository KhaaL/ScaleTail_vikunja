`# Make sure you replace SERVICE.`

# Vikunja with Tailscale Sidecar Configuration

This Docker Compose configuration sets up [Vikunja](https://github.com/go-vikunja/vikunja) with Tailscale as a sidecar container. 


## SERVICE

`[SERVICE](LINK TO PAFE OF MAINTAINER) information about service...`

[Vikunja](https://github.com/go-vikunja/vikunja) is the Todo-app to organize your life.


## Configuration Overview

In this setup, the `tailscale-SERVICE` service runs Tailscale, which manages secure networking for the SERVICE. The `SERVICE` service utilizes the Tailscale network stack via Docker's `network_mode: service:` configuration. This setup ensures that SERVICE's service is only accessible through the Tailscale network (or locally, if preferred), providing an extra layer of security and privacy for your SERVICE.

## Files to check

Please check the following contents for validity as some variables need to be defined upfront.

- `.env` // This files hold the main parts
- `./config/serve.json` // This file requires a service port of the app to be defined
++appconfig for app configurations for OICD.
