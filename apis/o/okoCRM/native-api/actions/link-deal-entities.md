# Link deal entities with OkoCRM

Links entities to a deal in OkoCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/[:lead_id]/link/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Link deal entities](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companies[][id]` | body | `string` | no | A company ID to link to the deal. |
| `contacts[][id]` | body | `string` | no | A contact ID to link to the deal. |
| `lead_id` | path | `number` | yes | The OkoCRM deal ID. |
