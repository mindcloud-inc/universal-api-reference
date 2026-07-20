# Instant: Sign Out Session by Refresh Token

Signs out an Instant session by refresh token.

```
DELETE https://connect.mindcloud.co/v1/universal/instant/latest/actions/sign-out-session-by-refresh-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instant/latest/actions/sign-out-session-by-refresh-token?connectionId=$CONNECTION_ID&refreshToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "refreshToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instant/latest/actions/sign-out-session-by-refresh-token?${params}`, {
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
| `refreshToken` | string | yes | Refresh token of the single session to revoke. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ok` | boolean | Whether the sign-out request succeeded. |

## Native endpoint

Through the native Instant API, this operation is `POST /admin/sign_out` (base URL `https://api.instantdb.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sign-out-session-by-refresh-token.md) for the provider-specific parameters and requirements.

