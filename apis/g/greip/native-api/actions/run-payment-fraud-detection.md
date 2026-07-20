# Run Payment Fraud Detection with Greip - Fraud Prevention

Runs payment fraud detection in Greip.

## Endpoint

- **Method:** `POST`
- **Path:** `/scoring/payment`
- **Base URL:** `https://greipapi.com`
- **Official documentation:** [Run Payment Fraud Detection](https://docs.greip.io/api-reference/endpoint/scoring/payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | Structured payment-fraud input object documented by Greip for the scoring request body. |
