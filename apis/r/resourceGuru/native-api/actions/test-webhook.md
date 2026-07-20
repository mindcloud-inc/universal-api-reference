# Test Webhook with Resource Guru

Tests a webhook in Resource Guru.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/:id/test`
- **Base URL:** `https://api.resourceguruapp.com/v1/{accountId}`
- **Official documentation:** [Test Webhook](https://resourceguruapp.com/docs/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Webhook ID. |
