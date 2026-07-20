# Test Webhook Submission with Lulu

Creates a test webhook submission in Lulu.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/{id}/test-submission/{topic}/`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Test Webhook Submission](https://api.lulu.com/docs/#tag/Webhooks/operation/test-webhook-submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Lulu webhook ID. |
| `topic` | path | `string` | yes | Webhook topic to test. |
