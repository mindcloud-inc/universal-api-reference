# Create Recipient Offline Payment with Trolley

Creates an offline payment for a recipient in Trolley.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/recipients/:id/offlinePayments`
- **Base URL:** `https://api.trolley.com`
- **Official documentation:** [Create Recipient Offline Payment](https://developers.trolley.com/api/#create-an-offline-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | no | Offline payment amount |
| `currency` | body | `string` | no | Offline payment currency |
| `id` | path | `string` | no | Recipient ID |
