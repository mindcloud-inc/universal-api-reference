# Delete Contact Note with Reamaze

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/:contactIdentifier/notes/:id`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Delete Contact Note](https://www.reamaze.com/api/delete_note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactIdentifier` | path | `string` | yes | Path parameter for email\|phone. |
| `id` | path | `string` | yes | Path parameter for id. |
