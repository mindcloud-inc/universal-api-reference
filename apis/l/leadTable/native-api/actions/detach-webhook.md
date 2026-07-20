# Detach webhook with LeadTable

## Endpoint

- **Method:** `POST`
- **Path:** `/removeWebhook`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [Detach webhook](https://docs.lead-table.com/leadtable-external-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `topic` | body | `list` | yes | Webhook topic to detach. Accepted values: `Change status`, `Delete lead`, `New lead`, `New table`, `Update lead`. |
| `layer` | body | `list` | yes | Scope level where the webhook is attached. Accepted values: `Agency`, `Customer`, `Table`. |
| `url` | body | `string` | yes | The exact webhook URL that should be detached. |
| `campaignID` | body | `string` | no | Campaign ID when detaching a table-level webhook. |
| `customerID` | body | `string` | no | Customer ID when detaching a customer-level webhook. |
