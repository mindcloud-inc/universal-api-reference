# Firebase: Get Access Token

Creates an access token for Firebase.

```
POST https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebase/latest/actions/get-access-token', {
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
      "access_token": "string",
      "expires_in": 1,
      "scope": "string",
      "token_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string | OAuth access token returned by Google. |
| `expires_in` | number | Lifetime of the access token in seconds. |
| `scope` | string | Granted OAuth scopes. |
| `token_type` | string | OAuth token type. |

## Native endpoint

Through the native Firebase API, this operation is `POST https://oauth2.googleapis.com/token` (base URL `https://firebase.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-access-token.md) for the provider-specific parameters and requirements.

