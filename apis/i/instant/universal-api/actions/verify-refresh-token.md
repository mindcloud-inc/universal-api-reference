# Instant: Verify Refresh Token

Verifies an Instant refresh token.

```
GET https://connect.mindcloud.co/v1/universal/instant/latest/actions/verify-refresh-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instant/latest/actions/verify-refresh-token?connectionId=$CONNECTION_ID&refreshToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "refreshToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instant/latest/actions/verify-refresh-token?${params}`, {
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
| `refreshToken` | string | yes | Refresh token to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user` | object | Instant user resolved from the refresh token. |

## Native endpoint

Through the native Instant API, this operation is `POST /runtime/auth/verify_refresh_token` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-refresh-token.md) for the provider-specific parameters and requirements.

