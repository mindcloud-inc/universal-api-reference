# Modify Endpoint with Control D

Updates an endpoint in Control D.

## Endpoint

- **Method:** `PUT`
- **Path:** `/devices/:deviceId`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Modify Endpoint](https://docs.controld.com/reference/put_devices-device-id)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | Device/Resolver ID |
| `name` | body | `string` | no | New Device name |
| `client_count` | body | `string` | no | Number of devices using this Endpoint |
| `profile_id` | body | `string` | no | Primary key of main profile to enforce on this device |
| `profile_id2` | body | `string` | no | Primary key of a second profile to enforce -1 to remove. |
| `stats` | body | `number` | no | Set analytics level on device. 0 = off, 1 = basic, 2 = full |
| `legacy_ipv4_status` | body | `number` | no | Set this to 1 to generate a legacy IPv4 (and IPv6) DNS resolver, 0 to remove existing one. |
| `learn_ip` | body | `number` | no | Enable or disable automatic IP learning and logging. 0 to disable, 1 to enable. |
| `restricted` | body | `number` | no | Make this device restricted. 0 to disable, 1 to enable. |
| `bump_tls` | body | `number` | no | Enable or disable experimental ECH support and TLS bumping |
| `desc` | body | `string` | no | Add a description or comment to the device |
| `ddns_status` | body | `number` | no | Status of public DDNS endpoint. 1 = enabled, 0 = disable. |
| `ddns_subdomain` | body | `string` | no | DDNS subdomain to expose the IP on |
| `ddns_ext_host` | body | `string` | no | DDNS hostname to query to learn new IPs |
| `ddns_ext_status` | body | `number` | no | Status of DDNS based IP learning. 0 to disable, 1 to enable. |
| `status` | body | `number` | no | Update device status. 0 - pending, 1 - active, 2 - soft disabled, 3 - hard disabled |
| `ctrld_custom_config` | body | `string` | no | ctrld .toml config file to deploy |
