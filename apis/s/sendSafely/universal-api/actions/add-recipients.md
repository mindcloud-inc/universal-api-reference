# SendSafely: Add Recipients



```
POST https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/add-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendSafely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/add-recipients" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/add-recipients', {
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
      "approvalRequired": true,
      "recipients": [
        {}
      ],
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalRequired` | boolean |  |
| `recipients` | array<object> |  |
| `response` | string |  |

## Native endpoint

Through the native SendSafely API, this operation is `PUT /package/:packageId/recipients/` (base URL `https://app.sendsafely.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-recipients.md) for the provider-specific parameters and requirements.

