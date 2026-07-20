# List Library Layers with Felt

Retrieves library layers from Felt.

## Endpoint

- **Method:** `GET`
- **Path:** `/library`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [List Library Layers](https://developers.felt.com/rest-api/api-reference/layers/layer-library)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | query | `list` | no | Which Felt library source to list. Accepted values: `All`, `Felt`, `Workspace`. |
