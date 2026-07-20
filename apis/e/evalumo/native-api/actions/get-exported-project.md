# Get Exported Project with Evalumo

Finds an exported project in Evalumo by ID or name.

## Endpoint

- **Method:** `GET`
- **Path:** `/exportedProject/:lookup`
- **Base URL:** `https://api.evalumo.com`
- **Official documentation:** [Get Exported Project](https://evalumo.apidocumentation.com/reference#tag/exported-project/GET/exportedProject/{idOrName})

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lookup` | path | `string` | yes | Exported project id, original project id, or project name lookup value. |
| `lineItemsToExpand` | query | `string` | no | Optional comma-separated line item sections to expand in the response. |
