# Upsert Link with Dub

Updates or creates a link in Dub by URL.

## Endpoint

- **Method:** `PUT`
- **Path:** `/links/upsert`
- **Base URL:** `https://api.dub.co`
- **Official documentation:** [Upsert Link](https://dub.co/docs/api-reference/links/upsert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Destination URL for the link. |
| `title` | body | `string` | no | Optional title for the link. |
