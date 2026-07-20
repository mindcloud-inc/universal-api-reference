# Reorder Folders with Instapaper

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1/folders/set_order`
- **Base URL:** `https://www.instapaper.com`
- **Official documentation:** [Reorder Folders](https://www.instapaper.com/developers/v1/full-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order` | body | `string` | yes | Comma-separated folder_id:position pairs including every folder you want ordered. |
