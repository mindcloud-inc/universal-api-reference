# List Calls with CallRail

Retrieves calls from CallRail.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/a/:account_id/calls.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [List Calls](https://apidocs.callrail.com/#listing-all-calls)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | The CallRail account ID. |
| `company_id` | query | `string` | no | Optional company ID to limit calls to one company. |
| `tracker_id` | query | `string` | no | Optional tracker ID to limit calls to one tracking number. |
| `date_range` | query | `string` | no | Optional preset date range such as recent or today. |
| `start_date` | query | `string` | no | Optional ISO 8601 start date for a custom date range. |
| `end_date` | query | `string` | no | Optional ISO 8601 end date for a custom date range. |
| `search` | query | `string` | no | Optional search text for customer, number, note, or source fields. |
| `fields` | query | `string` | no | Optional comma-separated additional call fields to return. |
