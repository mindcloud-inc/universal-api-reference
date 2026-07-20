# Lookup Custom Fields with IPLocate

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/:ip`
- **Base URL:** `https://iplocate.io/api`
- **Official documentation:** [Lookup Custom Fields](https://www.iplocate.io/docs/ip-intelligence-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | path | `string` | yes | IPv4 or IPv6 address to look up. |
| `include` | query | `string` | yes | Comma-separated list of fields or nested fields to return. |
