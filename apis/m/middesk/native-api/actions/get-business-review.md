# Retrieve a review for a business with Middesk

Retrieves a business review from Middesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/businesses/:business_id/review`
- **Base URL:** `https://api.middesk.com/v1`
- **Official documentation:** [Retrieve a review for a business](https://docs.middesk.com/reference/businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | path | `string` | yes | ID of the business whose review you want to retrieve. |
