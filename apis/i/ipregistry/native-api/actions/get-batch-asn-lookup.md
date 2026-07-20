# Get Batch ASN Lookup with Ipregistry

## Endpoint

- **Method:** `GET`
- **Path:** `/:asns`
- **Base URL:** `https://api.ipregistry.co`
- **Official documentation:** [Get Batch ASN Lookup](https://ipregistry.co/docs/endpoints#batch-as)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asns` | path | `string` | yes | Comma-separated list of up to 16 Autonomous System Numbers. |
| `fields` | query | `string` | no | Optional response filter applied to each ASN result item. |
