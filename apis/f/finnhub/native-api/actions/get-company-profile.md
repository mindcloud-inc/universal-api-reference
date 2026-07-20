# Get Company Profile with Finnhub

Retrieves a company profile from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock/profile2`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [Get Company Profile](https://finnhub.io/docs/api#company-profile2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | no | Company symbol, such as AAPL. |
| `isin` | query | `string` | no | Optional ISIN identifier for the company. |
| `cusip` | query | `string` | no | Optional CUSIP identifier for the company. |
