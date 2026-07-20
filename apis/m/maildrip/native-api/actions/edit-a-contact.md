# Edit a contact with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts/{contact_id}`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Edit a contact](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | ID of the contact to edit |
| `name` | body | `string` | no | — |
| `groups[]` | body | `array<string>` | no | Send multiple values as a array. |
