# Tableau Cloud: Update Workbook Connections

Updates workbook connections in Tableau Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-workbook-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-workbook-connections" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-workbook-connections', {
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

Through the native Tableau Cloud API, this operation is `PUT /sites/site-id/workbooks/workbook-id/connections` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workbook-connections.md) for the provider-specific parameters and requirements.

