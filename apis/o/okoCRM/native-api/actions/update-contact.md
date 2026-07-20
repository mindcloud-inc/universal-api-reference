# Update contact with OkoCRM

Updates an existing contact in OkoCRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/[:contact_id]/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Update contact](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `number` | yes | The OkoCRM contact ID. |
| `emails[][email]` | body | `string` | no | One email address to attach to the contact. |
| `name` | body | `string` | no | Updated contact full name. |
| `phones[][phone]` | body | `string` | no | One phone number to attach to the contact. |
