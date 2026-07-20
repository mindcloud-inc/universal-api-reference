# Update Link with lc.cx

Updates an existing short link in lc.cx.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/links/update/:id`
- **Base URL:** `https://api.lc.cx/v1`
- **Official documentation:** [Update Link](https://dev.lc.cx)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the link to update. |
| `rfc_validation` | query | `boolean` | no | Whether to validate the destination URL against the RFC format. |
| `tld_validation` | query | `boolean` | no | Whether to validate the destination URL top-level domain. |
| `destination` | body | `string` | no | The new destination URL for the shortlink. |
| `tags[]` | body | `array<string>` | no | Tag IDs to attach to the shortlink. Use an empty array to remove all tags. |
| `note` | body | `string` | no | An optional note for the shortlink. |
