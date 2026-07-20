# Create contact with OkoCRM

Creates a new contact in OkoCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Create contact](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[][email]` | body | `string` | no | One email address to attach to the contact. |
| `name` | body | `string` | yes | Contact full name. |
| `phones[][phone]` | body | `string` | no | One phone number to attach to the contact. |
