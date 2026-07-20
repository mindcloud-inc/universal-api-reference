# Resend Tracker Webhook Events with Ship24

Resends webhook events for an existing Ship24 tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/trackers/:trackerId/webhook-events/resend`
- **Base URL:** `https://api.ship24.com`
- **Official documentation:** [Resend Tracker Webhook Events](https://docs.ship24.com/tracking-api-reference/#/operations/resend-webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackerId` | path | `string` | yes | Ship24 tracker ID returned when the tracker was created. |
