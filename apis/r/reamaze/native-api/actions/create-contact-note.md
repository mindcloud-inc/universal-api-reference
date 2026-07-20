# Create Contact Note with Reamaze

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactIdentifier/notes`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [Create Contact Note](https://www.reamaze.com/api/post_notes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactIdentifier` | path | `string` | yes | Path parameter for email\|phone. |
| `body` | body | `string` | yes | Body payload field documented on https://www.reamaze.com/api/post_notes. |
