# Attach webhook with LeadTable

## Endpoint

- **Method:** `POST`
- **Path:** `/attachWebhook`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [Attach webhook](https://docs.lead-table.com/leadtable-external-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignID` | body | `string` | no | Campaign ID when attaching a table-level webhook. |
| `customerID` | body | `string` | no | Customer ID when attaching a customer-level webhook. |
| `url` | body | `string` | yes | The webhook URL to attach. |
| `topic` | body | `list` | yes | Webhook topic to attach. Accepted values: `Change status`, `Delete lead`, `New lead`, `New table`, `Update lead`. |
| `layer` | body | `list` | yes | Scope level where the webhook should be attached. Accepted values: `Agency`, `Customer`, `Table`. |
