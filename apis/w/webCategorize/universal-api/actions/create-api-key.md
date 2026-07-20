# WebCategorize: Create API Key



```
POST https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/create-api-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebCategorize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/create-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/create-api-key', {
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
      "createddAt": "2026-05-07T12:00:00.000Z",
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createddAt` | date | API key creation timestamp. Field name is spelled createddAt in the official schema. |
| `key` | string | API key value returned by WebCategorize. |

## Native endpoint

Through the native WebCategorize API, this operation is `POST /keys` (base URL `https://app.webcategorize.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-api-key.md) for the provider-specific parameters and requirements.

