# Issue Refund with Paycove

Issues a refund in Paycove.

## Endpoint

- **Method:** `POST`
- **Path:** `issue-refund`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Issue Refund](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `charge_id` | body | `string` | no | The charge ID to refund. |
| `refund_amount` | body | `string` | no | Optional partial refund amount. |
