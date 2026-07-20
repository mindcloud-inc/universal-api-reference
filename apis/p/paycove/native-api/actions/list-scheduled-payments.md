# List Scheduled Payments with Paycove

Retrieves scheduled payments from Paycove.

## Endpoint

- **Method:** `GET`
- **Path:** `scheduled-payments`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [List Scheduled Payments](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_due_date` | query | `date` | no | Filter scheduled payments due on or before this date. |
| `start_due_date` | query | `date` | no | Filter scheduled payments due on or after this date. |
