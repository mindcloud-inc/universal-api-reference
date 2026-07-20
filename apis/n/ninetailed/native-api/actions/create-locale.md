# Create Locale with Ninetailed

## Endpoint

- **Method:** `POST`
- **Path:** `/spaces/:space_id/environments/:environment_id/locales`
- **Base URL:** `https://api.contentful.com`
- **Official documentation:** [Create Locale](https://www.contentful.com/developers/docs/references/content-management-api/#/reference/locales/locale)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `string` | yes | Contentful space ID. |
| `environment_id` | path | `string` | yes | Contentful environment ID. |
| `name` | body | `string` | yes | Human-readable locale name. |
| `code` | body | `string` | yes | Locale code, for example en-GB. |
| `fallbackCode` | body | `string` | no | Fallback locale code, or null when no fallback should apply. |
