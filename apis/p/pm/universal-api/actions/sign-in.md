# 5pm: Sign In

Signs in to 5pm and returns a session ID.

```
GET https://connect.mindcloud.co/v1/universal/pm/latest/actions/sign-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 5pm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pm/latest/actions/sign-in?connectionId=$CONNECTION_ID&login=%7B%7Bcredentials.login%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "login": "{{credentials.login}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pm/latest/actions/sign-in?${params}`, {
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
| `login` | string | yes | 5pm login used for the authentication signIn call. Default: `{{credentials.login}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sessionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sessionId` | string | 5pm session token returned by signIn. |

## Native endpoint

Through the native 5pm API, this operation is `GET /service/get/authentication/signIn` (base URL `{{credentials.workspaceUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sign-in.md) for the provider-specific parameters and requirements.

