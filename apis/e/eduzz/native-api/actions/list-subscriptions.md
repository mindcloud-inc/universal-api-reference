# List Subscriptions with Eduzz

Retrieves subscription details from Eduzz for a date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/myeduzz/v1/subscriptions`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [List Subscriptions](https://developers.eduzz.com/reference/api/get-myeduzz-v1-subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | yes | Include subscriptions through this date. |
| `filterBy` | query | `string` | yes | Eduzz date field to filter subscriptions by. |
| `startDate` | query | `string` | yes | Include subscriptions from this date onward. |
