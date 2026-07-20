# List Checkout Form Elements with Ticket Tailor

Retrieves checkout form elements from Ticket Tailor.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/checkout_forms/:checkout_form_id/elements`
- **Base URL:** `https://api.tickettailor.com`
- **Official documentation:** [List Checkout Form Elements](https://developers.tickettailor.com/docs/api/get-checkout-form-elements-by-custom-form-id/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `checkout_form_id` | path | `string` | yes | Ticket Tailor checkout form ID. |
