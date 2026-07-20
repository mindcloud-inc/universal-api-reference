# Get SMS Pricing with Mocean API

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/2/account/pricing?mocean-resp-format=json&mocean-type=sms`
- **Base URL:** `https://rest.moceanapi.com`
- **Official documentation:** [Get SMS Pricing](https://moceanapi.com/docs#account-pricing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mocean-delimiter` | query | `string` | no | Optional CSV delimiter. |
| `mocean-mcc` | query | `string` | no | Optional mobile country code filter. |
| `mocean-mnc` | query | `string` | no | Optional mobile network code filter. |
