# Get ASN Lookup with Ipregistry

## Endpoint

- **Method:** `GET`
- **Path:** `/:asn`
- **Base URL:** `https://api.ipregistry.co`
- **Official documentation:** [Get ASN Lookup](https://ipregistry.co/docs/endpoints#single-as)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asn` | path | `string` | yes | Autonomous System Number to look up, for example `AS15169`. |
| `fields` | query | `string` | no | Optional response filter for ASN lookup results. |
