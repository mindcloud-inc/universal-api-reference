# Create Locale with Makeswift

Creates a new locale for a site in Makeswift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/locales`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Create Locale](https://docs.makeswift.com/developer/reference/api/locales/create-locale)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | body | `string` | yes | Site ID where the locale will be created. |
| `locale` | body | `string` | yes | Locale code (for example en-US). |
