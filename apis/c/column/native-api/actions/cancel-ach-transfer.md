# Cancel ACH Transfer with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/transfers/ach/:ach_transfer_id/cancel`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Cancel ACH Transfer](https://column.com/docs/api/#ach-transfer/cancel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ach_transfer_id` | path | `string` | yes | ID of the ACH transfer to cancel. |
