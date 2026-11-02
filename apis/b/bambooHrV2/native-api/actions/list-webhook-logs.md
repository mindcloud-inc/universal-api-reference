# List Webhook Logs with BambooHR

Lists webhook logs from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/webhooks/:id/log`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Webhook Logs](https://documentation.bamboohr.com/reference/list-webhook-logs)

## Requirements

- **OAuth scopes:** `webhooks`
- **scope:** `webhooks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The webhook ID to get logs about. |
