# Create Webhook with Slottable

Creates a new webhook in Slottable.

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/webhooks`
- **Base URL:** `https://slottable.app/api/v1`
- **Official documentation:** [Create Webhook](https://slottable.app/docs/p/integrations-and-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Company id returned by Slottable token details. |
| `url` | body | `string` | yes | Target URL that Slottable should call. |
| `model` | body | `string` | yes | Slottable model name to subscribe (for example Contact). |
