# SendSafely: Create Subdirectory



```
POST https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/create-subdirectory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendSafely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/create-subdirectory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/create-subdirectory', {
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
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native SendSafely API, this operation is `PUT /package/:packageId/directory/:directoryId/subdirectory/` (base URL `https://app.sendsafely.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subdirectory.md) for the provider-specific parameters and requirements.

