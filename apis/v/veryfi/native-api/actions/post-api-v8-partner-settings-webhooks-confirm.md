# Confirm a webhook with Veryfi

Confirms a webhook in Veryfi.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v8/partner/settings/webhooks/confirm`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Confirm a webhook](https://docs.veryfi.com/api/settings/confirm-a-webhook/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Possible values: non-empty and <= 2083 characters |
| `secret` | body | `string` | yes | Possible values: non-empty |
