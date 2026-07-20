# Starburst Galaxy: List catalog schema discoveries



```
GET https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-catalog-schema-discoveries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starburst Galaxy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-catalog-schema-discoveries?connectionId=$CONNECTION_ID&catalogId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "catalogId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starburstGalaxy/latest/actions/list-catalog-schema-discoveries?${params}`, {
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
| `catalogId` | string | yes | Starburst Galaxy catalog ID. Docs also support URL-encoded lookup expressions such as name=value. |
| `latest` | boolean | no | Whether to return only the latest catalog schema discovery result. |

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
          "createdAt": "2026-05-07T12:00:00.000Z",
          "errors": [
            "string"
          ],
          "schemaDiscoveryId": "string",
          "status": "string"
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
| `nextPageToken` | string | The next page token to use or empty string if there are no more pages. |
| `result[].catalogId` | string | Catalog ID. |
| `result[].createdAt` | date | Time when schema discovery was created. |
| `result[].errors` | array<string> | Errors that prevented schema discovery from finishing. |
| `result[].schemaDiscoveryId` | string | Schema discovery ID. |
| `result[].status` | string | Schema discovery status. |

## Native endpoint

Through the native Starburst Galaxy API, this operation is `GET /public/api/v1/catalog/{catalogId}/schemaDiscovery` (base URL `https://mindcloud.galaxy.starburst.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-catalog-schema-discoveries.md) for the provider-specific parameters and requirements.

