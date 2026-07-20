# Quiltt: Check Session Token



```
GET https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/check-session-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quiltt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/check-session-token?connectionId=$CONNECTION_ID&sessionToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/check-session-token?${params}`, {
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
| `sessionToken` | string | yes | Session token to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "environmentId": "string",
      "expiration": 1,
      "expiresAt": "string",
      "token": "string",
      "userId": "string",
      "userUuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `environmentId` | string |  |
| `expiration` | number |  |
| `expiresAt` | string |  |
| `token` | string |  |
| `userId` | string |  |
| `userUuid` | string |  |

## Native endpoint

Through the native Quiltt API, this operation is `GET https://auth.quiltt.io/v1/users/session` (base URL `https://api.quiltt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-session-token.md) for the provider-specific parameters and requirements.

