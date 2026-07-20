# Create Webhook with WEBLUCY

Creates a new webhook in WEBLUCY.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://apps.weblucy.com/api/site`
- **Official documentation:** [Create Webhook](https://websitebuilder.docs.apiary.io/#reference/webhooks/list-and-create/create-new-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events[]` | body | `array<string>` | yes | The webhook events to subscribe to. |
| `secret` | body | `string` | yes | The webhook secret used to sign events. |
| `target` | body | `string` | yes | The webhook destination URL. |
