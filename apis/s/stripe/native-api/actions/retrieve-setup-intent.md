# Retrieve SetupIntent with Stripe

## Endpoint

- **Method:** `GET`
- **Path:** `setup_intents/:setupIntent`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Retrieve SetupIntent](https://docs.stripe.com/api/setup_intents/retrieve)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setupIntent` | path | `string` | yes | Stripe SetupIntent ID returned by the completed setup-mode Checkout Session, for example seti_... |
