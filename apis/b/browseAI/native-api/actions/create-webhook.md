# Create Webhook with Browse AI

Creates a webhook in Browse AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/robots/:robotId/webhooks`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [Create Webhook](https://developers.browse.ai/v2#webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `hookUrl` | body | `string` | yes | Webhook URL |
| `eventType` | body | `list` | yes | Accepted values: `tableExportFinishedSuccessfully`, `taskCapturedDataChanged`, `taskFinished`, `taskFinishedSuccessfully`, `taskFinishedWithError`. |
