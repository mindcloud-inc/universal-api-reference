# Create Webhook with EZICHEQ

Creates a webhook in EZICHEQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/v1`
- **Base URL:** `https://api.ezicheq.com`
- **Official documentation:** [Create Webhook](https://developer.ezicheq.com/docs/endpoints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `kind` | body | `string` | yes |
| `url` | body | `string` | yes |
