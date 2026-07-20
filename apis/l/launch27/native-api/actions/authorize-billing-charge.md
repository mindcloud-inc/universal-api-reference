# Authorize Billing Charge with Launch27

Authorizes a billing charge in Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `setup/billing/authorize_charge`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [Authorize Billing Charge](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | Billing token to authorize. |
| `stripe_setup_intent_id` | body | `string` | yes | Stripe setup intent ID to pair with the authorization call. |
