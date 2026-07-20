# Bulk Update Reader Documents with Readwise

Updates multiple documents in Readwise Reader.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/bulk_update/`
- **Base URL:** `https://readwise.io`
- **Official documentation:** [Bulk Update Reader Documents](https://readwise.io/reader_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updates` | body | `list<object>` | yes | List of update objects. Each item must include id and may include title, author, summary, published_date, image_url, seen, location, category, tags, or notes. |
