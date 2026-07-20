# Update Contact with Octadesk

Updates an existing contact in Octadesk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:id`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Contact](https://developers.octadesk.com/reference/updatecontactinfobyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Customer email. |
| `id` | path | `string` | yes | Contact ID from Octadesk. |
| `name` | body | `string` | no | Customer name. |
