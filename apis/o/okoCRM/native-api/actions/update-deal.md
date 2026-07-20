# Update deal with OkoCRM

Updates an existing deal in OkoCRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads/[:lead_id]/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Update deal](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `budget` | body | `string` | no | Updated deal budget. |
| `lead_id` | path | `number` | yes | The OkoCRM deal ID. |
| `name` | body | `string` | no | Updated deal name. |
| `stages_id` | body | `string` | no | Updated stage ID. |
