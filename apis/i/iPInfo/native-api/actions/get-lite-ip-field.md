# Get Lite IP Field with IPInfo

## Endpoint

- **Method:** `GET`
- **Path:** `/lite/:ip/:field`
- **Base URL:** `https://api.ipinfo.io`
- **Official documentation:** [Get Lite IP Field](https://ipinfo.io/developers/lite-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | path | `string` | yes | IPv4 or IPv6 address to look up. |
| `field` | path | `string` | yes | Lite field path to return, for example country_code or asn. |
