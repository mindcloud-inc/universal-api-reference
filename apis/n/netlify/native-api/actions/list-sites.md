# List Sites with Netlify

## Endpoint

- **Method:** `GET`
- **Path:** `/sites`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [List Sites](https://open-api.netlify.com/#operation/listSites)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | — |
| `filter` | query | `list<string>` | no | Accepted values: `all`, `guest`, `owner`. |
