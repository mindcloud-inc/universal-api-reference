# Get All Widgets with Favro

Retrieves widgets from Favro.

## Endpoint

- **Method:** `GET`
- **Path:** `/widgets`
- **Base URL:** `https://favro.com/api/v1`
- **Official documentation:** [Get All Widgets](https://favro.com/developer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archived` | query | `boolean` | no | Return archived widgets when true. |
| `collectionId` | query | `string` | no | Filter widgets by collection ID. |
