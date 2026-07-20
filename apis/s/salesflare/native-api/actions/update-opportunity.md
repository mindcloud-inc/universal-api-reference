# Update Opportunity with Salesflare

## Endpoint

- **Method:** `PUT`
- **Path:** `opportunities/:id`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [Update Opportunity](https://api.salesflare.com/docs#/Opportunities/putOpportunitiesId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `close_date` | body | `date` | no | The date the opportunity was closed. |
| `id` | path | `number` | yes | The Salesflare opportunity ID. |
| `stage` | body | `number` | no | The Salesflare stage ID. |
| `value` | body | `number` | no | The monetary value of the opportunity. |
