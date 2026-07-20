# Pipedream: Get a new access token

Creates a new OAuth access token in Pipedream.

```
POST https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-new-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-new-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pipedream/latest/actions/get-a-new-access-token', {
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
      "accessToken": "string",
      "createdAt": 1,
      "expiresIn": 1,
      "scope": "string",
      "tokenType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string |  |
| `createdAt` | number |  |
| `expiresIn` | number |  |
| `scope` | string |  |
| `tokenType` | string |  |

## Native endpoint

Through the native Pipedream API, this operation is `POST /oauth/token` (base URL `https://api.pipedream.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-new-access-token.md) for the provider-specific parameters and requirements.

