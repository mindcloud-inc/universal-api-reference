# List Content Items (Preview) with Agility CMS

Retrieves preview content items from Agility CMS.

## Endpoint

- **Method:** `GET`
- **Path:** `/:guid/preview/:locale/list/:referenceName`
- **Base URL:** `https://api.aglty.io`
- **Official documentation:** [List Content Items (Preview)](https://api.aglty.io/swagger/v2/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceName` | path | `string` | yes | The lowercase content list reference name, for example posts or categories. |
