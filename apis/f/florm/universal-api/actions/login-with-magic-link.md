# Florm: Login With Magic Link

Logs into Florm with a magic link.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/login-with-magic-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/login-with-magic-link?connectionId=$CONNECTION_ID&guid=string&code=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "string",
  "code": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/login-with-magic-link?${params}`, {
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
| `guid` | string | yes | GUID of the Florm magic-link challenge. |
| `code` | number | yes | 4-digit code from the Florm magic link email. |
| `language` | string | no | Language code for the Florm login flow. Default: `ru`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessToken": "string",
      "expiresAccessToken": 1,
      "expiresRefreshToken": 1,
      "refreshToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string | Session access token returned by Florm. |
| `expiresAccessToken` | number | Minutes until the access token expires. |
| `expiresRefreshToken` | number | Minutes until the refresh token expires. |
| `refreshToken` | string | Session refresh token returned by Florm. |

## Native endpoint

Through the native Florm API, this operation is `PUT /v1/auth/magic-links` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/login-with-magic-link.md) for the provider-specific parameters and requirements.

