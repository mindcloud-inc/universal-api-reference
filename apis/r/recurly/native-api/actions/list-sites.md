# List Sites with Recurly

## Endpoint

- **Method:** `GET`
- **Path:** `/sites`
- **Base URL:** `https://v3.recurly.com`
- **Official documentation:** [List Sites](https://recurly.com/developers/api/v2021-02-25/#operation/list_sites)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Filter by one or more site IDs. |
| `state` | query | `string` | no | Filter sites by state. Accepted values: `0`, `1`. |
