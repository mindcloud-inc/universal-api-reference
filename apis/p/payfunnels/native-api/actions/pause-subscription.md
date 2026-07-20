# Pause Subscription with Payfunnels

Updates a subscription by pausing it in Payfunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscriptions/pause`
- **Base URL:** `https://api.payfunnels.com`
- **Official documentation:** [Pause Subscription](https://api.payfunnels.com/api/docs/#pause-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `behavior` | body | `string` | yes | How the paused subscription behaves. |
| `chargeUnpaidInvoice` | body | `boolean` | no | Charge unpaid invoices when resuming from a temporary pause. |
| `id` | body | `string` | yes | Subscription ID. |
| `resumeAt` | body | `number` | no | UNIX timestamp to resume automatically. |
