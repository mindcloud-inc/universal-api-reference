# Update Contact with Systeme.io

Updates an existing contact in Systeme.io.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/contacts/:id`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Update Contact](https://developer.systeme.io/reference/api_contacts_id_patch-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact identifier. |
