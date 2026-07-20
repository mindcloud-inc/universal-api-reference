# Update Link with Rebrandly

Updates an existing link in Rebrandly.

## Endpoint

- **Method:** `POST`
- **Path:** `/links/:id`
- **Base URL:** `https://api.rebrandly.com/v1`
- **Official documentation:** [Update Link](https://developers.rebrandly.com/docs/update-a-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the branded short link to update. |
| `destination` | body | `string` | yes | New destination URL for the branded short link. |
| `title` | body | `string` | yes | New title for the branded short link. |
| `favourite` | body | `boolean` | yes | Whether the branded short link should be marked as favourite. |
