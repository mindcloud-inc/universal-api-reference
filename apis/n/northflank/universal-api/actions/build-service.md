# Northflank: Build service

Starts a new build for a Northflank service.

```
POST https://connect.mindcloud.co/v1/universal/northflank/latest/actions/build-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Northflank `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/northflank/latest/actions/build-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/northflank/latest/actions/build-service', {
  method: 'POST',
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
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Northflank API, this operation is `POST /projects/{projectId}/services/{serviceId}/build` (base URL `https://api.northflank.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/build-service.md) for the provider-specific parameters and requirements.

