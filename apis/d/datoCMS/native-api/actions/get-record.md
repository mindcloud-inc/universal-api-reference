# Get Record with DatoCMS

## Endpoint

- **Method:** `GET`
- **Path:** `/items/:itemId`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Get Record](https://www.datocms.com/docs/content-management-api/resources/item/self)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | — |
| `nested` | query | `boolean` | no | For Modular Content, Structured Text and Single Block fields. If set, returns full payload for nested blocks instead of IDs. |
| `version` | query | `string` | no | Whether to return the currently published version (`published`) or latest available (`current`, default). |
