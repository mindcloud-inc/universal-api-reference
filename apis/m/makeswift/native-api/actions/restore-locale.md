# Restore Locale with Makeswift

Restores a deleted locale in Makeswift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/locales/:localeIdOrCode/restore`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Restore Locale](https://docs.makeswift.com/developer/reference/api/locales/restore-locale)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `localeIdOrCode` | path | `string` | yes | Locale ID or code to restore. |
| `siteId` | query | `string` | yes | The site ID containing the locale. |
