# Delete Widget with Favro

Deletes an existing widget from Favro.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/widgets/:widgetCommonId`
- **Base URL:** `https://favro.com/api/v1`
- **Official documentation:** [Delete Widget](https://favro.com/developer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | query | `string` | no | Delete the widget from one collection only when provided. |
| `widgetCommonId` | path | `string` | yes | The widget common ID to delete. |
