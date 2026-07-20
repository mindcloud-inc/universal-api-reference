# Tableau Cloud: Query Data Sources

Retrieves a list of data sources from Tableau Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-data-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-data-sources?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "contentUrl": "https://example.com",
      "createdAt": "string",
      "description": "string",
      "encryptExtracts": "string",
      "hasExtracts": "string",
      "id": "string",
      "isCertified": "string",
      "name": "Ava Chen",
      "type": "string",
      "updatedAt": "string",
      "webpageUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentUrl` | string | Data source content URL. |
| `createdAt` | string | Creation timestamp. |
| `description` | string | Data source description. |
| `encryptExtracts` | string | Whether extracts are encrypted. |
| `hasExtracts` | string | Whether the data source has extracts. |
| `id` | string | Data source ID. |
| `isCertified` | string | Whether the data source is certified. |
| `name` | string | Data source name. |
| `type` | string | Data source type. |
| `updatedAt` | string | Last update timestamp. |
| `webpageUrl` | string | Data source web URL. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `GET /sites/site-id/datasources` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/query-data-sources.md) for the provider-specific parameters and requirements.

