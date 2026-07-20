# List List Items with LEADTEX

Retrieves list items from a LEADTEX list.

## Endpoint

- **Method:** `POST`
- **Path:** `/getListItems?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [List List Items](https://docs.leadteh.ru/rabota-s-api/spiski/elementy-spiska/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schema_id` | body | `string` | yes | ID of the list schema whose items should be returned. |
