# Add Webhook with Klenty

Creates a webhook in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/zapier/hooks`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Add Webhook](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_45a9638c98)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_url` | body | `string` | yes | Webhook destination URL. |
| `event` | body | `string` | yes | Webhook event name. |
