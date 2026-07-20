# Update Webhook with Klenty

Updates an existing webhook in Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/update`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Update Webhook](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_c5f05d6ef7)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_id` | body | `string` | yes | Webhook id to update. |
| `event` | body | `string` | yes | Webhook event to trigger on. |
| `subscription_url` | body | `string` | yes | Webhook destination URL. |
