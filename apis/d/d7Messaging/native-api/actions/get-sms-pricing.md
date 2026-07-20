# Get SMS Pricing with D7 Messaging

Retrieves SMS pricing from D7 Messaging.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/v1/sms/pricing`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Get SMS Pricing](https://d7networks.com/docs/sms/pricing/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country_iso` | query | `string` | no | Optional ISO alpha-2 country code to return pricing for a single country. Leave empty to fetch pricing for all countries. |
