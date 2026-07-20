# List Secret Status with One-Time Secret

Retrieves statuses for multiple secrets in One-Time Secret.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/secret/status`
- **Base URL:** `https://us.onetimesecret.com`
- **Official documentation:** [List Secret Status](https://api.onetimesecret.com/doc/api-v2/operation/operation-v2_listsecretstatus)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifiers[]` | body | `array<string>` | yes | Secret identifiers to check status for. |
