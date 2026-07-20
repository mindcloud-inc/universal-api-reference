# Update Short Link with Ayrshare

Updates a short link in Ayrshare.

## Endpoint

- **Method:** `PUT`
- **Path:** `/links/:id`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [Update Short Link](https://www.ayrshare.com/docs/apis/links/update-short-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Ayrshare short link ID to update. |
| `url` | body | `string` | yes | New destination URL for the short link. |
