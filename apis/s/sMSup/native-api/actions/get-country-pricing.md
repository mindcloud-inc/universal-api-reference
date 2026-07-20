# Get Country Pricing with SMSup

## Endpoint

- **Method:** `POST`
- **Path:** `/api/3.0/account/pricing/sms/get-country-pricing`
- **Base URL:** `https://api.gateway360.com`
- **Official documentation:** [Get Country Pricing](https://app.smsup.es/api/3.0/docs/account/get-pricing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_code` | body | `string` | no | A country in ISO alpha-2 format. If omitted, all countries are returned. |
