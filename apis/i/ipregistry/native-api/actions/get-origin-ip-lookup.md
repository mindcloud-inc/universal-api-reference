# Get Origin IP Lookup with Ipregistry

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://api.ipregistry.co`
- **Official documentation:** [Get Origin IP Lookup](https://ipregistry.co/docs/endpoints#origin-ip)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Optional response filter. Origin IP lookups also include user-agent data. |
| `hostname` | query | `boolean` | no | Set to true to include a fresh reverse DNS hostname lookup. |
