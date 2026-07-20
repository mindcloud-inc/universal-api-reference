# Create Contact Note with Clio Grow

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/{contact_id}/notes`
- **Base URL:** `https://api.clio.com/grow`
- **Official documentation:** [Create Contact Note](https://docs.developers.clio.com/clio-grow/api-reference/#tag/Contacts/operation/ContactNote%23create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The unique identifier for the contact. |
| `data.subject` | body | `string` | yes | Subject line of the note. Maximum length: 255. |
| `data.body` | body | `string` | yes | Body content of the note. Maximum length: 65535. |
