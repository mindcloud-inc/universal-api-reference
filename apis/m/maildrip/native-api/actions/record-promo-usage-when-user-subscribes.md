# Record promo usage when user subscribes with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/promo/record-usage`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Record promo usage when user subscribes](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `planId` | body | `string` | yes | The plan ID the user subscribed to |
| `pricePaid` | body | `number` | yes | The actual price the user paid |
| `currency` | body | `string` | no | — |
