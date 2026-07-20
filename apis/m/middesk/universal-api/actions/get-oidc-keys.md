# Middesk: Retrieve OIDC public keys

Retrieves OIDC public keys from Middesk.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-oidc-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-oidc-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-oidc-keys?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "keys": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `keys` | array<object> | OIDC public keys used to validate Middesk webhook JWTs. |

## Native endpoint

Through the native Middesk API, this operation is `GET /webhooks/oidc_keys` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oidc-keys.md) for the provider-specific parameters and requirements.

