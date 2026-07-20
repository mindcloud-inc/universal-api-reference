# Replace Contact with Octadesk

Replaces an existing contact in Octadesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Replace Contact](https://developers.octadesk.com/reference/updatecontactbyid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Customer email. |
| `id` | path | `string` | yes | Contact ID from Octadesk. |
| `name` | body | `string` | yes | Customer name. |
