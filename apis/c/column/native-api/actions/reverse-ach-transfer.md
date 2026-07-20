# Reverse ACH Transfer with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/transfers/ach/:ach_transfer_id/reverse`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Reverse ACH Transfer](https://column.com/docs/api/#ach-transfer/reverse)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ach_transfer_id` | path | `string` | yes | ID of the original ACH transfer to reverse. |
| `reason` | body | `string` | yes | Reason for the ACH reversal. |
| `description` | body | `string` | no | Internal description for the reversal transfer. |
