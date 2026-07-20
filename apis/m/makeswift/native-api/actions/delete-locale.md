# Delete Locale with Makeswift

Deletes an existing locale from Makeswift.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/locales/:localeIdOrCode`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Delete Locale](https://docs.makeswift.com/developer/reference/api/locales/delete-locale)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `localeIdOrCode` | path | `string` | yes | Locale ID or code to delete. |
| `siteId` | query | `string` | yes | The site ID containing the locale. |
