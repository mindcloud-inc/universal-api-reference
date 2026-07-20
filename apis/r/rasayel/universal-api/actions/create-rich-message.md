# Rasayel: Create Rich Message

Creates a rich message in Rasayel.

```
POST https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/create-rich-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rasayel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/create-rich-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rasayel/latest/actions/create-rich-message', {
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
      "clientMutationId": "string",
      "message": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientMutationId` | string |  |
| `message` | object |  |

## Native endpoint

Through the native Rasayel API, this operation is `POST /` (base URL `https://api.rasayel.io/api/graphql`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-rich-message.md) for the provider-specific parameters and requirements.

