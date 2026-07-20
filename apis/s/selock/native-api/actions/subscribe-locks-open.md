# Subscribe Lock Open Events with Selock

## Endpoint

- **Method:** `POST`
- **Path:** `/zaiper/subscribe/locks_open/`
- **Base URL:** `https://selock.co/api/v1`
- **Official documentation:** [Subscribe Lock Open Events](https://selock.co/en/docs/selock-zapier-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Webhook URL that Selock should call. |
