# Tableau Cloud: Update Data Source Now

Refreshes a data source in Tableau Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-data-source-now
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tableau Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-data-source-now" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tableauCloud/latest/actions/update-data-source-now', {
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
      "createdAt": "string",
      "extractRefreshJob": {
        "datasource": {
          "id": "string",
          "name": "Ava Chen"
        }
      },
      "id": "string",
      "mode": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Job creation timestamp. |
| `extractRefreshJob.datasource.id` | string | Data source ID. |
| `extractRefreshJob.datasource.name` | string | Data source name. |
| `id` | string | Job ID. |
| `mode` | string | Job execution mode. |
| `type` | string | Job type. |

## Native endpoint

Through the native Tableau Cloud API, this operation is `POST /sites/site-id/datasources/datasource-id/refresh` (base URL `https://us-east-1.online.tableau.com/api/3.28`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-data-source-now.md) for the provider-specific parameters and requirements.

