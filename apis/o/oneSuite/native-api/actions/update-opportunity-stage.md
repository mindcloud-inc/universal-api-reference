# Update Opportunity Stage with OneSuite

Updates an opportunity stage in OneSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/opportunities/:opportunity_id/stage`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Update Opportunity Stage](https://rest-api.onesuite.io/#update-opportunity-stage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunity_id` | path | `string` | yes | Opportunity ID from the update-opportunity-stage docs. |
| `stage.id` | body | `string` | yes | Stage object ID from the update-opportunity-stage docs. |
