# Submit Mandate Consent with TrueLayer

Submits mandate consent in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/mandates/:id/authorization-flow/actions/consent`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Submit Mandate Consent](https://docs.truelayer.com/reference/submit-consent-mandate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer mandate ID. |
