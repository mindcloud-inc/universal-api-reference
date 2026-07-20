# Get Customer Billing Provider Configurations with Metronome

Retrieves customer billing provider configurations from Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/getCustomerBillingProviderConfigurations`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Get Customer Billing Provider Configurations](https://docs.metronome.com/api-reference/customers/fetch-billing-provider-configurations-for-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `string` | yes | The customer ID. |
