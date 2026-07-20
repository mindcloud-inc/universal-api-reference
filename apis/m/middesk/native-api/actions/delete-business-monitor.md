# Delete a monitor for a business with Middesk

Deletes a business monitor from Middesk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/businesses/:business_id/monitor`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Delete a monitor for a business](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business whose monitor you want to delete. |
