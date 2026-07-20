# Delete Short Link with TLY Link Shortener

Deletes an existing short link from TLY Link Shortener.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/link`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Delete Short Link](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `short_url` | body | `string` | yes | The short URL to delete. |
