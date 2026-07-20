# Create Webhook with Tremendous

Creates a new webhook in Tremendous.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://testflight.tremendous.com/api/v2`
- **Official documentation:** [Create Webhook](https://developers.tremendous.com/reference/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook receiver URL |
