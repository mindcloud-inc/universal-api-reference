# Delete Recipient Offline Payment with Trolley

Deletes a recipient offline payment from Trolley.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/recipients/:recipientId/offlinePayments/:offlinePaymentId`
- **Base URL:** `https://api.trolley.com`
- **Official documentation:** [Delete Recipient Offline Payment](https://developers.trolley.com/api/#delete-an-offline-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offlinePaymentId` | path | `string` | no | Offline payment ID |
| `recipientId` | path | `string` | no | Recipient ID |
