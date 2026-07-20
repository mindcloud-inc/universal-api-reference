# Unsubscribe Lock Close Events with Selock

## Endpoint

- **Method:** `POST`
- **Path:** `/zaiper/unsubscribe/locks_close/`
- **Base URL:** `https://selock.co/api/v1`
- **Official documentation:** [Unsubscribe Lock Close Events](https://selock.co/en/docs/selock-zapier-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Webhook URL that Selock should stop calling. |
