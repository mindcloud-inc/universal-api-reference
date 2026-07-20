# Update Tag with Wooxy

Updates an existing tag in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/tags/update`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Update Tag](https://wooxy.com/api-documentation/tags/update-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | body | `string` | yes | Existing tag name to update. |
| `name` | body | `string` | no | New tag name. |
| `description` | body | `string` | no | Updated tag description. |
