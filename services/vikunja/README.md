`# Make sure you replace SERVICE.`

# Vikunja with Tailscale Sidecar Configuration

This Docker Compose configuration sets up [Vikunja](https://github.com/go-vikunja/vikunja) with Tailscale as a sidecar container. 


## Vikunja

[Vikunja](https://github.com/go-vikunja/vikunja) Vikunja is a self-hosted to-do list application that lets you organize tasks, projects, and notes in a flexible and collaborative way.


## Configuration Overview

In this setup, the `tailscale-vikunja` service runs Tailscale, which manages secure networking for Vikunja. The `vikunja` service utilizes the Tailscale network stack via Docker's `network_mode: service:` configuration. This setup ensures that SERVICE's service is only accessible through the Tailscale network (or locally, if preferred), providing an extra layer of security and privacy for your Vikunja instance.


## Files to check

Please check the following contents for validity as some variables need to be defined upfront.

- `.env` // This files hold the main parts
- `./config/serve.json` // This file requires a service port of the app to be defined
`./appconfig/config  // for app configurations for OICD.`
