# List Campaigns with Budgets.ai

## Endpoint

- **Method:** `POST`
- **Path:** `/api-product/incoming-webhook/fetch-all-campaigns`
- **Base URL:** `https://myapiconnect.com`
- **Official documentation:** [List Campaigns](https://crm.budgets.ai/dashboard/api-center/incoming)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `state` | body | `string` | yes | Use running, paused, or all to choose which campaigns Budgets.ai returns. |
