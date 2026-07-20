# Subscribe New Orders with Selock

## Endpoint

- **Method:** `POST`
- **Path:** `/zaiper/subscribe/orders/`
- **Base URL:** `https://selock.co/api/v1`
- **Official documentation:** [Subscribe New Orders](https://selock.co/en/docs/selock-zapier-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Webhook URL that Selock should call. |
| `order_fields[]` | body | `array<string>` | no | Optional list of order creation statuses: not confirmed, confirmed, busy, canceled, all. |
