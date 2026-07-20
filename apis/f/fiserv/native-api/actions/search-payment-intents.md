# Search Payment Intents with Fiserv

Finds payment intents in Fiserv by filter criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/payment_intents/search`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [Search Payment Intents](https://isvportal.fiserv.com/docs/payments-api#operation/search_payment_intent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `requestBody` | body | `object` | yes | JSON request body from the official payment intent search schema. |
