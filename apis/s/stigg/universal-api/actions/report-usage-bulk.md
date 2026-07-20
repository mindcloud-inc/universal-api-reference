# Stigg: Report Usage Bulk



```
POST https://connect.mindcloud.co/v1/universal/stigg/latest/actions/report-usage-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stigg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stigg/latest/actions/report-usage-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stigg/latest/actions/report-usage-bulk', {
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
      "id": "string",
      "items": [
        {}
      ],
      "message": "string",
      "refId": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `items` | array<object> |  |
| `message` | string |  |
| `refId` | string |  |
| `status` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Stigg API, this operation is `POST /graphql` (base URL `https://api.stigg.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/report-usage-bulk.md) for the provider-specific parameters and requirements.

