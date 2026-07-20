# Create On-Demand Subscription Invoice with Billwerkplus

Creates an on-demand invoice for a Billwerkplus subscription.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscription/:handle/invoice`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [Create On-Demand Subscription Invoice](https://docs.frisbii.com/reference/createsubscriptioninvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | path | `string` | yes | Subscription handle. |
| `handle` | body | `string` | yes | Unique invoice handle. |
| `instant` | body | `boolean` | no | Process the invoice immediately. |
| `plan_manual` | body | `boolean` | no | Generate plan order lines manually for the invoice. |
| `plan_period_from` | body | `string` | no | Service period start for manually generated plan lines. |
| `plan_period_to` | body | `string` | no | Service period end for manually generated plan lines. |
