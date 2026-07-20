# Create Card with Favro

Creates a new card in Favro.

## Endpoint

- **Method:** `POST`
- **Path:** `/cards`
- **Base URL:** `https://favro.com/api/v1`
- **Official documentation:** [Create Card](https://favro.com/developer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `columnId` | body | `string` | yes | The column ID where the card will be created. |
| `name` | body | `string` | yes | The card name. |
| `widgetCommonId` | body | `string` | yes | The widget common ID where the card will be created. |
