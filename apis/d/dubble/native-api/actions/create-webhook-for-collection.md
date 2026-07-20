# Create Webhook for Collection with Dubble

Creates a new webhook for a collection in Dubble.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/:collectionId`
- **Base URL:** `https://api.dubble.so/v1`
- **Official documentation:** [Create Webhook for Collection](https://dubble.readme.io/reference/post_webhooks-collectionid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | The ID of the collection |
| `name` | body | `string` | no | Optional name for the webhook |
| `target_url` | body | `string` | yes | The URL where the webhook will send data |
| `triggers[]` | body | `array<string>` | yes | Trigger events for the webhook |
