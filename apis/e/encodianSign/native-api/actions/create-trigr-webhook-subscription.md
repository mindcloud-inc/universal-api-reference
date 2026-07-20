# Create Trigr Webhook Subscription with Encodian - Sign

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Trigr/ManageWebHook`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Create Trigr Webhook Subscription](https://api.apps-encodian.com/swagger/Sign/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callbackUrl` | body | `string` | yes | Webhook callback URL that Encodian Trigr should call. |
| `title` | body | `string` | yes | Title of the Encodian Trigr webhook subscription. |
| `description` | body | `string` | no | Description of the Trigr webhook subscription purpose. |
