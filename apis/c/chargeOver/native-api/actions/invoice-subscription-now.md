# Invoice Subscription Now with ChargeOver

Invoices an existing subscription immediately in ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/package/:package_id/_action/invoice`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Invoice Subscription Now](https://developer.chargeover.com/docs/api/invoice-a-subscription-now/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `package_id` | path | `number` | yes | The ChargeOver subscription ID. |
