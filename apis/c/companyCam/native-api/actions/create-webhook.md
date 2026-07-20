# Create Webhook with CompanyCam

Creates a new webhook in CompanyCam.

## Endpoint

- **Method:** `POST`
- **Path:** `webhooks`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Create Webhook](https://docs.companycam.com/reference/createwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopes` | body | `list<string>` | no | See all available scopes here: https://docs.companycam.com/docs/webhooks-1 Send multiple values as a array. |
| `enabled` | body | `boolean` | no | Format: `toggle`. |
| `url` | body | `string` | no | — |
