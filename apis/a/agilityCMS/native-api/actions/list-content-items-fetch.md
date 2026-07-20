# List Content Items (Fetch) with Agility CMS

Retrieves published content items from Agility CMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/:guid/fetch/:locale/list/:referenceName`
- **Base URL:** `https://api.aglty.io`
- **Official documentation:** [List Content Items (Fetch)](https://api.aglty.io/swagger/v2/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceName` | path | `string` | yes | The lowercase content list reference name, for example posts or categories. |
