# Delete Webhook with Klenty

Deletes an existing webhook from Klenty.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/delete`
- **Base URL:** `https://api.klenty.com/apis/v1/user/{username}`
- **Official documentation:** [Delete Webhook](https://support.klenty.com/en/articles/8193937-klenty-s-post-apis#h_ef5aaf283e)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookId` | body | `string` | yes | Webhook id to delete. |
