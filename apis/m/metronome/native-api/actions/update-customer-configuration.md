# Update Customer Configuration with Metronome

Updates a customer configuration in Metronome.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/customers/:customer_id/updateConfig`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Update Customer Configuration](https://docs.metronome.com/api-reference/customers/update-a-customer-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The customer ID. |
| `leave_stripe_invoices_in_draft` | body | `boolean` | no | Whether to leave Stripe invoices in draft. |
