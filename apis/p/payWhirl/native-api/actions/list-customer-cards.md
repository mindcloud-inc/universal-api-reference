# List Customer Cards with PayWhirl

Retrieves a customer's cards from PayWhirl.

## Endpoint

- **Method:** `GET`
- **Path:** `/cards/{customer_id}`
- **Base URL:** `https://api.paywhirl.com`
- **Official documentation:** [List Customer Cards](https://api.paywhirl.com/#charges)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `number` | yes | The PayWhirl customer ID. |
