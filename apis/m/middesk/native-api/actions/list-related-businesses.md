# List related businesses with Middesk

Retrieves related businesses from your Middesk account.

## Endpoint

- **Method:** `GET`
- **Path:** `/businesses/:business_id/related_businesses`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [List related businesses](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business whose related businesses you want to list. |
