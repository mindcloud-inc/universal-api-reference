# Create Widget with Favro

Creates a new widget in Favro.

## Endpoint

- **Method:** `POST`
- **Path:** `/widgets`
- **Base URL:** `https://favro.com/api/v1`
- **Official documentation:** [Create Widget](https://favro.com/developer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | body | `string` | yes | The collection ID where the widget will be created. |
| `name` | body | `string` | yes | The name of the widget. |
| `type` | body | `string` | yes | The widget type to create. |
