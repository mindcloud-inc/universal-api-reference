# Clarifai: Create Concepts by User App ID

Creates concepts in Clarifai.

```
POST https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-concepts-by-user-app-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clarifai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-concepts-by-user-app-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clarifai/latest/actions/create-concepts-by-user-app-id', {
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
      "appId": "string",
      "createdAt": "string",
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "userId": "string",
      "value": 1,
      "visibility": {
        "gettable": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string |  |
| `createdAt` | string |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `userId` | string |  |
| `value` | number |  |
| `visibility.gettable` | number |  |

## Native endpoint

Through the native Clarifai API, this operation is `POST /v2/concepts` (base URL `https://api.clarifai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-concepts-by-user-app-id.md) for the provider-specific parameters and requirements.

