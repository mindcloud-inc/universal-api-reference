# Get Locale with Makeswift

Retrieves a locale from Makeswift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/locales/:localeIdOrCode`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Get Locale](https://docs.makeswift.com/developer/reference/api/locales/get-locale)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `localeIdOrCode` | path | `string` | yes | Locale ID or locale code. |
| `siteId` | query | `string` | yes | The site ID containing the locale. |
