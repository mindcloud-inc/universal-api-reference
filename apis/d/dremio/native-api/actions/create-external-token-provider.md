# Create External Token Provider with Dremio

Creates a new external token provider in Dremio.

## Endpoint

- **Method:** `POST`
- **Path:** `/external-token-providers`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Create External Token Provider](https://docs.dremio.com/dremio-cloud/api/external-token-providers/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `provider` | body | `object` | yes |
| `type` | body | `string` | yes |
