# ns8-headscale

[Headscale](https://headscale.net/stable/) is an open source, self-hosted implementation of the Tailscale control server.

## Install

Instantiate the module with:

    add-module ghcr.io/mrmarkuz/headscale:latest 1

The output of the command will return the instance name.
Output example:

    {"module_id": "headscale1", "image_name": "headscale", "image_url": "ghcr.io/mrmarkuz/headscale:latest"}

## Configure

- Set an FQDN and browse to `https://<FQDN>/web`

- Get an API key:

      runagent -m headscale1 podman exec -ti headscale-app headscale apikeys create

- Setup the API key and the FQDN in headscale UI

- It's possible to secure the /web path for headscale1-web by adding address restrictions in the HTTP routes


## Uninstall

To uninstall the instance:

    remove-module --no-preserve headscale1

