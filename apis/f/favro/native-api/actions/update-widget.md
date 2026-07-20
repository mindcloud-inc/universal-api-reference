# Update Widget with Favro

Updates an existing widget in Favro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/widgets/:widgetCommonId`
- **Base URL:** `https://favro.com/api/v1`
- **Official documentation:** [Update Widget](https://favro.com/developer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | The widget color. |
| `name` | body | `string` | no | The new widget name. |
| `widgetCommonId` | path | `string` | yes | The widget common ID to update. |
