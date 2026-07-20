# Update Custom Domain with condoo

Updates an existing custom domain in condoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/domains/{domain_id}`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [Update Custom Domain](https://trk.condoo.systems/en/api-documentation/domains)

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
| `domain_id` | path | `number` | yes | Required custom domain ID. |
| `host` | body | `string` | no | Optional custom domain host. |
