# Create Identity Provider with Dremio

Creates a new identity provider in Dremio.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity-providers`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Create Identity Provider](https://docs.dremio.com/dremio-cloud/api/identity-providers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `provider` | body | `object` | yes |
| `type` | body | `string` | yes |
