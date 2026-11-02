# Get Webhook with BambooHR

Retrieves webhook from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/webhooks/:id`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [Get Webhook](https://documentation.bamboohr.com/reference/get-webhook)

## Requirements

- **OAuth scopes:** `webhooks`
- **scope:** `webhooks` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The webhook ID to retrieve. |
