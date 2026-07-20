# Create Webhook with Reach360

Creates a new webhook in Reach360.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.reach360.com`
- **Official documentation:** [Create Webhook](https://www.articulatesupport.com/article/Reach-360-Webhooks-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetUrl` | body | `string` | yes | The destination URL for webhook events. |
| `events` | body | `list<string>` | yes | The webhook events to subscribe to. |
| `sharedSecret` | body | `string` | no | Optional shared secret used to sign webhook requests. |
| `apiVersion` | body | `string` | no | Optional API version to use when sending webhook events. |
