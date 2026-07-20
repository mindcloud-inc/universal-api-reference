# Create Webhook with Roger

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.rogerroger.io`
- **Official documentation:** [Create Webhook](https://developer.rogerroger.io/webhooks/set-up-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook destination URL. |
| `description` | body | `string` | no | Optional webhook description. |
