# Validate Phone Number with Numverify

Retrieves validation details for a phone number from Numverify.

## Endpoint

- **Method:** `GET`
- **Path:** `/validate`
- **Base URL:** `https://apilayer.net/api`
- **Official documentation:** [Validate Phone Number](https://docs.apilayer.com/numverify/docs/numverify-api-v-1-0-0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | Phone number to validate. |
| `country_code` | query | `string` | no | ISO 3166-1 alpha-2 country code for national-format numbers. |
