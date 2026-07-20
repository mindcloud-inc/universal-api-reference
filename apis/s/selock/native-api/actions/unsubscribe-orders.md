# Unsubscribe New Orders with Selock

## Endpoint

- **Method:** `POST`
- **Path:** `/zaiper/unsubscribe/orders/`
- **Base URL:** `https://selock.co/api/v1`
- **Official documentation:** [Unsubscribe New Orders](https://selock.co/en/docs/selock-zapier-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Webhook URL that Selock should stop calling. |
