# LoginRadius: Invalidate Access Token

Invalidates an access token in LoginRadius.

```
DELETE https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/invalidate-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoginRadius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/invalidate-access-token?connectionId=$CONNECTION_ID&accessToken=seeded-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accessToken": "seeded-access-token"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loginRadius/latest/actions/invalidate-access-token?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessToken` | string | yes | Access Token to invalidate. Example: `seeded-access-token`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `preventRefresh` | boolean | no | Whether to prevent refresh-token based renewal. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isPosted": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isPosted` | boolean | Whether LoginRadius invalidated the supplied access token. |

## Native endpoint

Through the native LoginRadius API, this operation is `GET /identity/v2/auth/access_token/invalidate` (base URL `https://api.loginradius.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invalidate-access-token.md) for the provider-specific parameters and requirements.

