# Update Opportunity with OneSuite

Updates an opportunity in OneSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/opportunities/:opportunity_id`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Update Opportunity](https://rest-api.onesuite.io/#update-opportunity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunity_id` | path | `string` | yes | Opportunity ID from the update-opportunity docs. |
| `name` | body | `string` | no | Updated opportunity name. |
