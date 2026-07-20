# Get All Cards with Favro

Retrieves cards from Favro.

## Endpoint

- **Method:** `GET`
- **Path:** `/cards`
- **Base URL:** `https://favro.com/api/v1`
- **Official documentation:** [Get All Cards](https://favro.com/developer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Return archived cards when true. |
| `widgetCommonId` | query | `string` | yes | The widget common ID whose cards should be listed. |
