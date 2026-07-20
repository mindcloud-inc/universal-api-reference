# List Customer Subscription Preferences with Customer.io

Retrieves subscription preferences for a customer in Customer.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers/:customer_id/subscription_preferences`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [List Customer Subscription Preferences](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPersonSubscriptionPreferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The ID of the customer to inspect. |
| `id_type` | query | `list<string>` | no | The type of identifier provided in Customer ID. Accepted values: `cio_id`, `email`, `id`. |
| `language` | query | `string` | no | The language tag to use for translated subscription-center content. |
