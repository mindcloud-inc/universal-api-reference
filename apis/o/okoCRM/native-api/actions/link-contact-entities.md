# Link contact entities with OkoCRM

Links entities to a contact in OkoCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/[:contact_id]/link/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Link contact entities](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companies[][id]` | body | `string` | no | A company ID to link to the contact. |
| `contact_id` | path | `number` | yes | The OkoCRM contact ID. |
| `leads[][id]` | body | `string` | no | A deal ID to link to the contact. |
