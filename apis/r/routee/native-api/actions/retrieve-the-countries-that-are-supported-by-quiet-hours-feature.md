# Retrieve the countries that are supported by Quiet Hours feature with Routee

Retrieves the countries that are supported by quiet hours feature from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/quietHours/countries/:language`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve the countries that are supported by Quiet Hours feature](https://docs.routee.net/reference/retrieve-the-countries-that-are-supported-by-the-quiet-hours-feature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | path | `string` | yes | The language code is ISO 639-1 format (el, en) that will be used to translate the country names. |
