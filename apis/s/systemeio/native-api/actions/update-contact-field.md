# Update Contact Field with Systeme.io

Updates an existing contact field in Systeme.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/contact_fields/:slug`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Update Contact Field](https://developer.systeme.io/reference/api_contact_fields_slug_patch-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `slug` | path | `string` | yes | Contact field slug. |
