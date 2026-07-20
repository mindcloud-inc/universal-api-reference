# Subscribe Order Changes with Selock

## Endpoint

- **Method:** `POST`
- **Path:** `/zaiper/subscribe/orders_change/`
- **Base URL:** `https://selock.co/api/v1`
- **Official documentation:** [Subscribe Order Changes](https://selock.co/en/docs/selock-zapier-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Webhook URL that Selock should call. |
| `order_change_fields[]` | body | `array<string>` | no | Optional list of order-change filters: not confirmed, confirmed, busy, canceled, date and time, price, paid, lock_key, comment, all. |
