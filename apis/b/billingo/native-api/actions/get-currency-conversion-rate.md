# Get Currency Conversion Rate with Billingo

Retrieves currency conversion rates from Billingo.

## Endpoint

- **Method:** `GET`
- **Path:** `/currencies`
- **Base URL:** `https://api.billingo.hu/v3`
- **Official documentation:** [Get Currency Conversion Rate](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Source currency code for the conversion rate. |
| `to` | query | `string` | yes | Target currency code for the conversion rate. |
| `date` | query | `date` | no | Optional conversion-rate date. |
