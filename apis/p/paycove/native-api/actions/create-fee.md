# Create Fee with Paycove

Creates a fee for a Paycove deal.

## Endpoint

- **Method:** `POST`
- **Path:** `deals/:crm_deal_id/fees`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [Create Fee](https://docs.paycove.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | no | Flat fee amount. |
| `crm_deal_id` | path | `string` | yes | The CRM deal ID that owns the fee. |
| `label` | body | `string` | yes | The fee label. |
| `percent` | body | `number` | no | Percentage fee amount. |
