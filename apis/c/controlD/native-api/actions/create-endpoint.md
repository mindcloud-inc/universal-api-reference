# Create Endpoint with Control D

Creates an endpoint in Control D.

## Endpoint

- **Method:** `POST`
- **Path:** `/devices`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Create Endpoint](https://docs.controld.com/reference/post_devices)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Device name |
| `client_count` | body | `string` | yes | Number of devices using this Endpoint |
| `profile_id` | body | `string` | yes | Primary key of main profile to enforce on this device |
| `profile_id2` | body | `string` | no | Primary key of a second profile to enforce |
| `icon` | body | `string` | yes | Device icon/type |
| `stats` | body | `number` | no | Set analytics level on device. 0 = off, 1 = basic, 2 = full |
| `legacy_ipv4_status` | body | `number` | no | Set this to 1 to generate a legacy IPv4 (and IPv6) DNS resolver. |
| `learn_ip` | body | `number` | no | Enable or disable automatic IP learning and logging. 0 to disable, 1 to enable. |
| `restricted` | body | `number` | no | Make this device restricted, only previously authorized IPs will be able to query against it |
| `desc` | body | `string` | no | Add a description or comment to the device |
| `ddns_status` | body | `number` | no | Status of DDNS endpoint that exposes last used IP. |
| `ddns_subdomain` | body | `string` | no | DDNS subdomain to expose the IP on |
| `ddns_ext_status` | body | `number` | no | Status of DDNS based IP learning |
| `ddns_ext_host` | body | `string` | no | DDNS hostname to query to learn new IPs |
| `remap_device_id` | body | `string` | no | Remap source device + client ID to a new device |
| `remap_client_id` | body | `string` | no | Remap source device + client ID to a new device |
