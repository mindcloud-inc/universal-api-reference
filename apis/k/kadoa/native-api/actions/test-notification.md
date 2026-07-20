# Test Notification with Kadoa

## Endpoint

- **Method:** `POST`
- **Path:** `/v5/notifications/test`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Test Notification](https://docs.kadoa.com/api-reference/notifications/test-notifications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventType` | body | `string` | yes | Event type to test |
| `workflowId` | body | `string` | no | Workflow ID for test context |
