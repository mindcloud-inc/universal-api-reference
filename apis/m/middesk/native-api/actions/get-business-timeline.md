# Retrieve timeline for a business with Middesk

Retrieves a business timeline from Middesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/businesses/:business_id/timeline`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Retrieve timeline for a business](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business whose timeline you want to retrieve. |
