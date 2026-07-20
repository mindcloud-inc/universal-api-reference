# Unsubscribe Order Changes with Selock

## Endpoint

- **Method:** `POST`
- **Path:** `/zaiper/unsubscribe/orders_change/`
- **Base URL:** `https://selock.co/api/v1`
- **Official documentation:** [Unsubscribe Order Changes](https://selock.co/en/docs/selock-zapier-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Webhook URL that Selock should stop calling. |
