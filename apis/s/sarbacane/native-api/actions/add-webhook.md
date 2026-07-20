# Add Webhook with Sarbacane

Creates a new webhook in Sarbacane.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [Add Webhook](https://developers.sarbacane.com/contacts/#add-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `displayName` | body | `string` | no | Webhook display name. |
| `kinds` | body | `string` | no | Webhook event kinds array. |
| `url` | body | `string` | no | Webhook destination URL. |
