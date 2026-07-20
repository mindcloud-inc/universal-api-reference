# Create Custom Domain with condoo

Creates a new custom domain in condoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/domains`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [Create Custom Domain](https://trk.condoo.systems/en/api-documentation/domains)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_index_url` | body | `string` | no | Optional custom index URL. |
| `custom_not_found_url` | body | `string` | no | Optional custom not-found URL. |
| `host` | body | `string` | yes | Required custom domain host. |
