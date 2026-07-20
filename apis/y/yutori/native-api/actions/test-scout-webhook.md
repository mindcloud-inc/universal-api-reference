# Test Scout Webhook with Yutori

Creates a test request for a Yutori scout webhook.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scouting/webhooks/test`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Test Scout Webhook](https://docs.yutori.com/reference/webhook)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `webhook_url` | body | `string` | yes |
| `webhook_format` | body | `string` | yes |
| `scout_id` | body | `string` | no |
