# EMnify: Retrieve Authentication Token

Retrieves an authentication token from EMnify.

```
POST https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-authentication-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EMnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-authentication-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eMnify/latest/actions/retrieve-authentication-token', {
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
      "authToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authToken` | string |  |

## Native endpoint

Through the native EMnify API, this operation is `POST /authenticate` (base URL `https://cdn.emnify.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-authentication-token.md) for the provider-specific parameters and requirements.

