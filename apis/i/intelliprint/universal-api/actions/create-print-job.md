# Intelliprint: Create Print Job



```
POST https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-print-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intelliprint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-print-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intelliprint/latest/actions/create-print-job', {
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
      "account": "string",
      "confirmed": true,
      "created": 1,
      "id": "string",
      "object": "string",
      "reference": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `confirmed` | boolean |  |
| `created` | number |  |
| `id` | string |  |
| `object` | string |  |
| `reference` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Intelliprint API, this operation is `POST /prints` (base URL `https://api.intelliprint.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-print-job.md) for the provider-specific parameters and requirements.

