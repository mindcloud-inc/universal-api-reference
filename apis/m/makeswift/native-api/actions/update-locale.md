# Update Locale with Makeswift

Updates an existing locale in Makeswift.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/locales/:localeIdOrCode`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Update Locale](https://docs.makeswift.com/developer/reference/api/locales/update-locale)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `localeIdOrCode` | path | `string` | yes | Locale ID or locale code to update. |
| `siteId` | query | `string` | yes | The site ID containing the locale. |
| `locale` | body | `string` | no | Updated locale code. |
| `domain` | body | `string` | no | Custom domain for this locale. |
| `pathPrefix` | body | `string` | no | Path prefix for this locale, e.g. /fr. |
