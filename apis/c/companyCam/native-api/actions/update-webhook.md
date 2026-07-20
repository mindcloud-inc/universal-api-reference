# Update Webhook with CompanyCam

Updates an existing webhook in CompanyCam.

## Endpoint

- **Method:** `PUT`
- **Path:** `webhooks/:id`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Update Webhook](https://docs.companycam.com/reference/updatewebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | — |
| `scopes` | body | `list<string>` | no | See all available scopes here: https://docs.companycam.com/docs/webhooks-1 Send multiple values as a array. |
| `enabled` | body | `boolean` | no | Format: `toggle`. |
| `id` | path | `string` | yes | — |
