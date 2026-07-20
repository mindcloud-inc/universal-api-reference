# Update Contact Book with Marketing Master IO

Updates an existing contact book in Marketing Master IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts/books/:book_id`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Update Contact Book](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `book_id` | path | `string` | yes | — |
| `name` | body | `string` | yes | Updated contact book name. |
