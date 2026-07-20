# Update Institution with PocketSmith

Updates a PocketSmith institution.

## Endpoint

- **Method:** `PUT`
- **Path:** `/institutions/:id`
- **Base URL:** `https://api.pocketsmith.com/v2`
- **Official documentation:** [Update Institution](https://developers.pocketsmith.com/reference/put_institutions-id-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency_code` | body | `string` | no | A new currency code for the institution. |
| `id` | path | `number` | yes | The unique identifier of the PocketSmith institution. |
| `title` | body | `string` | no | A new title for the institution. |
