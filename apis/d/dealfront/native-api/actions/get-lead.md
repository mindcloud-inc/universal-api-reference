# Get Lead with Dealfront

Retrieves a lead from Dealfront.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:account_id/leads/:lead_id`
- **Base URL:** `https://api.leadfeeder.com`
- **Official documentation:** [Get Lead](https://docs.leadfeeder.com/api/#get-a-specific-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | ID of the account that owns the lead. |
| `lead_id` | path | `string` | yes | ID of the lead to retrieve. |
