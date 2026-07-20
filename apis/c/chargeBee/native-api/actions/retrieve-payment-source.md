# Retrieve Payment Source with ChargeBee

Retrieves a payment source from ChargeBee.

## Endpoint

- **Method:** `GET`
- **Path:** `payment_sources/:payment_source_id`
- **Base URL:** `https://{baseUrl}.chargebee.com/api/v2/`
- **Official documentation:** [Retrieve Payment Source](https://apidocs.chargebee.com/docs/api/payment-sources/retrieve-a-payment-source)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payment_source_id` | path | `string` | yes | The Chargebee payment source identifier. |
