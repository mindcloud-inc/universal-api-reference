# Create Opportunity with Close

Creates a new opportunity in Close.

## Endpoint

- **Method:** `POST`
- **Path:** `/opportunity/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Create Opportunity](https://developer.close.com/resources/opportunities/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | body | `string` | yes | Lead ID for this opportunity. |
| `note` | body | `string` | no | Opportunity description note. |
| `status_id` | body | `string` | no | Opportunity status ID. |
| `value` | body | `number` | no | Opportunity value. |
