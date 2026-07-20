# Tableau Cloud: Update Data Source

Updates an existing data source in Tableau Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-data-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-data-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-data-source', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Tableau Cloud API, this operation is `PUT /sites/site-id/datasources/datasource-id` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-data-source.md) for the provider-specific parameters and requirements.

