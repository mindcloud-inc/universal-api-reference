# Update Follow-Up with ManyReach

Updates an existing follow-up in ManyReach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.manyreach.com/api/v2/followups/:id`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Update Follow-Up](https://api.manyreach.com/api#v2/tag/followup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Followup ID. |
| `waitMin` | body | `string` | no | Updated wait duration amount. |
| `waitUnits` | body | `string` | no | Updated wait duration units. |
