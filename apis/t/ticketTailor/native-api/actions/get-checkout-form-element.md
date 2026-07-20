# Get Checkout Form Element with Ticket Tailor

Retrieves a checkout form element from Ticket Tailor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/checkout_forms/:checkout_form_id/elements/:checkout_form_element_id`
- **Base URL:** `https://api.tickettailor.com`
- **Official documentation:** [Get Checkout Form Element](https://developers.tickettailor.com/docs/api/get-checkout-form-element-by-id/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkout_form_id` | path | `string` | yes | Ticket Tailor checkout form ID. |
| `checkout_form_element_id` | path | `string` | yes | Ticket Tailor checkout form element ID. |
