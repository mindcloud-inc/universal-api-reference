# Get Webhook Delivery with SonarQube

Retrieves a webhook delivery from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/webhooks/delivery`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Get Webhook Delivery](https://sonarcloud.io/web_api/api/webhooks/delivery)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deliveryId` | query | `string` | yes | Webhook delivery ID. Required by /api/webhooks/delivery. |
