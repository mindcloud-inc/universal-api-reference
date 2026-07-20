# Create an API Key with Algolia

Creates a new API key in Algolia.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/keys`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Create an API Key](https://www.algolia.com/doc/rest-api/search/add-api-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `acl[]` | body | `array<string>` | yes | Permissions this API key can use. |
| `description` | body | `string` | no | Description to help identify this API key. |
| `validity` | body | `number` | no | Duration in seconds before the API key expires. |
| `indexes[]` | body | `array<string>` | no | Index names or patterns this API key can access. |
| `maxHitsPerQuery` | body | `number` | no | Maximum number of results this key can retrieve in one query. |
| `maxQueriesPerIPPerHour` | body | `number` | no | Maximum number of API requests allowed per IP per hour. |
| `queryParameters` | body | `string` | no | Query parameters to append when this key is used. |
| `referers[]` | body | `array<string>` | no | Allowed HTTP referrers for this API key. |
