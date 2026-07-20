# Update Opportunity with Close

Updates an existing opportunity in Close.

## Endpoint

- **Method:** `PUT`
- **Path:** `/opportunity/:id/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Update Opportunity](https://developer.close.com/resources/opportunities/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique Opportunity ID. |
| `note` | body | `string` | no | Opportunity description note. |
| `status_id` | body | `string` | no | Opportunity status ID. |
| `value` | body | `number` | no | Opportunity value. |
