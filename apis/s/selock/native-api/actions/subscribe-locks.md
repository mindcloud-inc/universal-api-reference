# Subscribe Lock Events with Selock

## Endpoint

- **Method:** `POST`
- **Path:** `/zaiper/subscribe/locks/`
- **Base URL:** `https://selock.co/api/v1`
- **Official documentation:** [Subscribe Lock Events](https://selock.co/en/docs/selock-zapier-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Webhook URL that Selock should call. |
