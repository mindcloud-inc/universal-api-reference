# Rownd Data Privacy: Create OIDC Client



```
POST https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-oidc-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rownd Data Privacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-oidc-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-oidc-client', {
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
      "client_id": "string",
      "grant_types": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "redirect_uris": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `client_id` | string | OIDC client ID. |
| `grant_types` | array<string> | Allowed OAuth grant types. |
| `id` | string | OIDC client identifier. |
| `name` | string | OIDC client display name. |
| `redirect_uris` | array<string> | Allowed redirect URIs. |

## Native endpoint

Through the native Rownd Data Privacy API, this operation is `POST /oidc-clients` (base URL `https://api.rownd.io/applications/{{credentials.appId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-oidc-client.md) for the provider-specific parameters and requirements.

