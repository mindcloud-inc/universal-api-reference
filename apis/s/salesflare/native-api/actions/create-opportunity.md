# Create Opportunity with Salesflare

## Endpoint

- **Method:** `POST`
- **Path:** `opportunities`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [Create Opportunity](https://api.salesflare.com/docs#/Opportunities/postOpportunities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account` | body | `number` | yes | The Salesflare account ID linked to the opportunity. |
| `close_date` | body | `date` | no | The date the opportunity was closed. |
| `value` | body | `number` | no | The monetary value of the opportunity. |
