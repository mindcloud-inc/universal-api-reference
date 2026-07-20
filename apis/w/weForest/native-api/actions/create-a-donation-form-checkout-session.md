# Create a donation form checkout session with WeForest

Creates a donation form checkout session in WeForest.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:id/checkout`
- **Base URL:** `https://api.weforest.org`
- **Official documentation:** [Create a donation form checkout session](https://docs.weforest.org/create-a-donation-form-checkout-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Donation form identifier from WeForest. |
| `items[]` | body | `array<object>` | yes | Array of donation items with productId and quantity. |
| `user` | body | `object` | yes | Donor user object with email and name. |
| `successUrl` | body | `string` | yes | URL to redirect to after successful checkout. |
| `cancelUrl` | body | `string` | no | URL to redirect to if checkout is cancelled. |
| `currency` | body | `string` | no | Checkout currency code. |
