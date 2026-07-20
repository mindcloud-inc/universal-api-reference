# Rownd Data Privacy: Create Magic Link



```
POST https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-magic-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-magic-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-magic-link', {
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
      "email": "ava@example.com",
      "id": "string",
      "link": "https://example.com",
      "phone": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Target email when present. |
| `id` | string | Magic link identifier when returned. |
| `link` | string | Generated magic link URL. |
| `phone` | string | Target phone when present. |
| `user_id` | string | Target Rownd user identifier. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `POST https://api.rownd.io/hub/auth/magic` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-magic-link.md) for the provider-specific parameters and requirements.

