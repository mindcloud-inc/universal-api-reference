# Update Locale with Ninetailed

## Endpoint

- **Method:** `PUT`
- **Path:** `/spaces/:spaceId/environments/:environmentId/locales/:localeId`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Update Locale](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/locales/locale)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Contentful space ID. |
| `environmentId` | path | `string` | yes | Contentful environment ID, such as master. |
| `localeId` | path | `string` | yes | Locale resource ID to update. |
| `version` | body | `number` | yes | Current Contentful locale version for X-Contentful-Version. |
| `name` | body | `string` | yes | Locale display name. |
| `code` | body | `string` | yes | Locale code, such as en-US. |
