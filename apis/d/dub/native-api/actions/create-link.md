# Create Link with Dub

Creates a link in Dub.

## Endpoint

- **Method:** `POST`
- **Path:** `/links`
- **Base URL:** `https://api.dub.co`
- **Official documentation:** [Create Link](https://dub.co/docs/api-reference/links/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Destination URL for the short link. |
| `title` | body | `string` | no | Optional title for the link. |
