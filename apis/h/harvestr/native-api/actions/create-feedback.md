# Create Feedback with Harvestr.io

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [Create Feedback](https://developers.harvestr.io/api/create-a-feedback-link-a-message-to-a-discovery/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messageId` | body | `string` | yes | The message ID to link the feedback to |
| `discoveryId` | body | `string` | yes | The discovery ID to link the feedback to |
| `score` | body | `number` | no | The feedback score (minimum 0) |
| `processMessage` | body | `boolean` | no | Mark the message as processed after creating the feedback |
