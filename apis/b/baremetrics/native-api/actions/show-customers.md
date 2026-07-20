# Show Customers with Baremetrics

Retrieves customers for a metric from Baremetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/metrics/:metric/customers`
- **Base URL:** `https://sandbox.baremetrics.com`
- **Official documentation:** [Show Customers](https://developers.baremetrics.com/reference/show-customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | query | `string` | yes | — |
| `end_date` | query | `string` | yes | — |
| `metric` | path | `string` | yes | You can see a list of available metrics [here](customer#) |
