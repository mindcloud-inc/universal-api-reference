# Create Activity with ForceManager

Creates a new activity in ForceManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities`
- **Official documentation:** [Create Activity](https://support.forcemanager.net/en/articles/8613478-entity-types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activity_date_time` | body | `date` | yes | Date and time of the activity. |
| `sales_rep_id` | body | `number` | yes | ID of the sales rep user this activity is created for. |
| `account_id` | body | `number` | yes | ID of the account this activity is assigned to. |
