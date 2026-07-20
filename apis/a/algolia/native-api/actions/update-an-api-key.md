# Update an API Key with Algolia

Updates an existing API key in Algolia.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1/keys/:key`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Update an API Key](https://www.algolia.com/doc/rest-api/search/update-api-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | path | `string` | yes | API key to update. |
| `acl[]` | body | `array<string>` | yes | Access control list permissions for the API key. |
| `description` | body | `string` | no | Description of the API key. |
| `validity` | body | `number` | no | Duration in seconds before the key expires. |
| `indexes[]` | body | `array<string>` | no | Restrict the API key to a set of indices. |
| `maxHitsPerQuery` | body | `number` | no | Maximum number of results returned per query. |
| `maxQueriesPerIPPerHour` | body | `number` | no | Maximum number of queries per IP address per hour. |
| `queryParameters` | body | `string` | no | Search parameters enforced by this API key. |
| `referers[]` | body | `array<string>` | no | Restrict the API key to specific HTTP referrers. |
