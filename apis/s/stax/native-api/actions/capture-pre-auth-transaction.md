# Capture Pre-Auth Transaction with Stax

Captures a pre-authorized transaction in Stax.

## Endpoint

- **Method:** `POST`
- **Path:** `/transaction/:transactionid/capture`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Capture Pre-Auth Transaction](https://docs.staxpayments.com/reference/capture-a-pre-auth-transaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactionid` | path | `string` | no | Pre-auth transaction identifier |
