# Lookup Bogon Status with IPLocate

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/:ip/privacy.is_bogon`
- **Base URL:** `https://iplocate.io/api`
- **Official documentation:** [Lookup Bogon Status](https://www.iplocate.io/docs/guides/bogons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | path | `string` | yes | IPv4 or IPv6 address to inspect. |
