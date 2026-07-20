# List Exported Projects with Evalumo

Retrieves exported project records from your Evalumo account.

## Endpoint

- **Method:** `GET`
- **Path:** `/exportedProject`
- **Base URL:** `https://api.evalumo.com`
- **Official documentation:** [List Exported Projects](https://evalumo.apidocumentation.com/reference#tag/exported-project/GET/exportedProject)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lineItemsToExpand` | query | `string` | no | Optional comma-separated line item sections to expand, for example TasksByItem or Takeoff. |
