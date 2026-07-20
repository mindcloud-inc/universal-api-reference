# List Content Items V1 (Fetch) with Agility CMS

Retrieves published content items from Agility CMS v1.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/:guid/fetch/:locale/list/:referenceName`
- **Base URL:** `https://api.aglty.io`
- **Official documentation:** [List Content Items V1 (Fetch)](https://api.aglty.io/swagger/v1/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceName` | path | `string` | yes | The lowercase content list reference name, for example posts or categories. |
