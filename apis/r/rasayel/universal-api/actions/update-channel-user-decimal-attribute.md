# Rasayel: Update Channel User Decimal Attribute

Updates a decimal attribute on a Rasayel channel user.

```
PUT https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/update-channel-user-decimal-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rasayel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/update-channel-user-decimal-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/update-channel-user-decimal-attribute', {
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
      "attrType": "string",
      "decimalValue": 1,
      "id": "string",
      "name": "Ava Chen",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attrType` | string |  |
| `decimalValue` | number |  |
| `id` | string |  |
| `name` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native Rasayel API, this operation is `POST /` (base URL `https://api.rasayel.io/api/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-channel-user-decimal-attribute.md) for the provider-specific parameters and requirements.

