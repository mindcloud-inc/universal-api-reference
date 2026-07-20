# Lookup Historical IP with IPLocate

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/:ip`
- **Base URL:** `https://iplocate.io/api`
- **Official documentation:** [Lookup Historical IP](https://www.iplocate.io/docs/ip-intelligence-api/historical-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip` | path | `string` | yes | IPv4 or IPv6 address to look up historically. |
| `at` | query | `string` | yes | Specific historical lookup date in YYYY-MM-DD format. |
