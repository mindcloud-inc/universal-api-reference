# Update Contact with SparrowDesk

Updates an existing contact in SparrowDesk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{{id}}`
- **Base URL:** `https://api.sparrowdesk.com/v1`
- **Official documentation:** [Update Contact](https://developer.sparrowdesk.com/rest-api/endpoints/contacts/id/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | body | `string` | no | Updated SparrowDesk company identifier. |
| `email` | body | `string` | no | Updated contact email. |
| `first_name` | body | `string` | no | Updated contact first name. |
| `id` | path | `number` | yes | SparrowDesk contact ID. |
| `last_name` | body | `string` | no | Updated contact last name. |
| `phone` | body | `string` | no | Updated contact phone number. |
