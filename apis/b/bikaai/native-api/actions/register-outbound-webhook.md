# Register Outbound Webhook with Bika.ai

Creates an outbound webhook in Bika.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/spaces/:spaceId/outgoing-webhooks`
- **Base URL:** `https://bika.ai/api/openapi/bika/v1`
- **Official documentation:** [Register Outbound Webhook](https://bika.ai/help/guide/developer/openapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Bika.ai workspace/space ID. |
| `eventType` | body | `string` | yes | Webhook event type such as ON_RECORD_CREATED. |
| `name` | body | `string` | yes | Webhook name. |
| `callbackURL` | body | `string` | yes | HTTPS URL that Bika.ai should call when the webhook event occurs. |
| `description` | body | `string` | no | Webhook description. |
