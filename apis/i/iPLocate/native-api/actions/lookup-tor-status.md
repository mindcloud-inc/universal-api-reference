# Lookup Tor Status with IPLocate

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/:ip/privacy.is_tor`
- **Base URL:** `https://iplocate.io/api`
- **Official documentation:** [Lookup Tor Status](https://www.iplocate.io/docs/guides/detect-vpn-and-proxies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | path | `string` | yes | IPv4 or IPv6 address to inspect. |
