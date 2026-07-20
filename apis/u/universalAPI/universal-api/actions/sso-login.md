# Universal API: SSO Login

Retrieves an SSO login URL from Universal API.

```
GET https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/sso-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universal API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/sso-login?connectionId=$CONNECTION_ID&redirectUri=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "redirectUri": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/sso-login?${params}`, {
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
| `redirectUri` | string | yes | Redirect URI used by the SSO login flow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Universal API API, this operation is `GET /api/sso/login` (base URL `https://api.prod.universalapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sso-login.md) for the provider-specific parameters and requirements.

