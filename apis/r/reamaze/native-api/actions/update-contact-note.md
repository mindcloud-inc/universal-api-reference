# Update Contact Note with Reamaze

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contactIdentifier/notes/:id`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Update Contact Note](https://www.reamaze.com/api/put_note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactIdentifier` | path | `string` | yes | Path parameter for email\|phone. |
| `id` | path | `string` | yes | Path parameter for id. |
| `body` | body | `string` | no | Body payload field documented on https://www.reamaze.com/api/put_note. |
