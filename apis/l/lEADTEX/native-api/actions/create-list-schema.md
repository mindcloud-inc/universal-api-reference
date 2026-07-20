# Create List Schema with LEADTEX

Creates a new list schema in LEADTEX.

## Endpoint

- **Method:** `POST`
- **Path:** `/createListSchema?api_token={apiKey}`
- **Base URL:** `https://app.leadteh.ru/api/v1`
- **Official documentation:** [Create List Schema](https://docs.leadteh.ru/rabota-s-api/spiski/schema-spiska/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | body | `object` | yes | Schema fields object keyed by field slug. |
| `is_menu` | body | `boolean` | yes | Whether to show the list in the LEADTEX interface menu. |
| `name` | body | `string` | yes | List schema name. |
