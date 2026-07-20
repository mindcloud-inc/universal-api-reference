# Delete OneLink Stats with TLY Link Shortener

Deletes stats for a OneLink in TLY Link Shortener.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/onelink/stat`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Delete OneLink Stats](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `short_url` | body | `string` | yes | The OneLink short URL whose stats should be deleted. |
