# List Checkout Session Line Items with Stripe

Retrieves line items for a Stripe checkout session.

## Endpoint

- **Method:** `GET`
- **Path:** `checkout/sessions/:session/line_items`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Checkout Session Line Items](https://docs.stripe.com/api/checkout/sessions/line_items)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session` | path | `string` | yes | Checkout Session identifier. |
| `limit` | query | `number` | no | Number of line items to return (1-100). |
| `starting_after` | query | `string` | no | Cursor for forward pagination. |
| `ending_before` | query | `string` | no | Cursor for reverse pagination. |
| `expand` | query | `list<string>` | no | Fields to expand in the response. |
