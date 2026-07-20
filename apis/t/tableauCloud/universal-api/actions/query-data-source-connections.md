# Tableau Cloud: Query Data Source Connections

Retrieves data source connections from Tableau Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-data-source-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-data-source-connections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/query-data-source-connections?${params}`, {
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
      "authenticationType": "string",
      "embedPassword": "string",
      "id": "string",
      "queryTaggingEnabled": "string",
      "serverAddress": "string",
      "serverPort": "string",
      "type": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticationType` | string | Authentication type. |
| `embedPassword` | string | Whether the password is embedded. |
| `id` | string | Connection ID. |
| `queryTaggingEnabled` | string | Whether query tagging is enabled. |
| `serverAddress` | string | Server address. |
| `serverPort` | string | Server port. |
| `type` | string | Connection type. |
| `userName` | string | User name. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `GET /sites/site-id/datasources/datasource-id/connections` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-data-source-connections.md) for the provider-specific parameters and requirements.

