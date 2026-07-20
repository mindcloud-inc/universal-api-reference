# Starburst Galaxy: List OpenSearch catalogs



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-open-search-catalogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-open-search-catalogs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-open-search-catalogs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageSize` | number | no | Page size, or 0 for the Starburst Galaxy API default. Current maximum is 100. Example: `100`. |
| `pageToken` | string | no | Pagination token returned by a previous Starburst Galaxy API response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "result": [
        {
          "catalogId": "string",
          "description": "string",
          "name": "Ava Chen",
          "readOnly": true,
          "validate": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string |  |
| `result[].catalogId` | string |  |
| `result[].description` | string |  |
| `result[].name` | string |  |
| `result[].readOnly` | boolean |  |
| `result[].validate` | boolean |  |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/catalogType/opensearch/catalog` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-open-search-catalogs.md) for the provider-specific parameters and requirements.

