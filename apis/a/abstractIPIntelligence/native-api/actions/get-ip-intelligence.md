# Get IP Intelligence with Abstract IP Intelligence

Retrieves IP intelligence from Abstract IP Intelligence.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://ip-intelligence.abstractapi.com/v1`
- **Official documentation:** [Get IP Intelligence](https://docs.abstractapi.com/api/ip-intelligence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ip_address` | query | `string` | no | IPv4 or IPv6 address to analyze. Leave blank to let Abstract infer the caller IP. |
| `fields` | query | `string` | no | Comma-separated top-level response sections to return Send multiple values as a string separated by `,`. |
