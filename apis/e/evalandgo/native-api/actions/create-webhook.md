# Create Webhook with Evalandgo

Creates a new webhook in Evalandgo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/webhooks`
- **Base URL:** `https://app.evalandgo.com`
- **Official documentation:** [Create Webhook](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1webhooks/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `questionnaire` | body | `string` | yes |
| `name` | body | `string` | no |
| `url` | body | `string` | no |
| `events[]` | body | `array<string>` | no |
