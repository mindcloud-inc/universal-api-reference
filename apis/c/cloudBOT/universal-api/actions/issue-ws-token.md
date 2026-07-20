# Cloud BOT: Issue WS Token

Issues a WebSocket token in Cloud BOT.

```
GET https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/issue-ws-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud BOT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/issue-ws-token?connectionId=$CONNECTION_ID&publicId=string&scopes%5B%5D=string&keys%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicId": "string",
  "scopes[]": "string",
  "keys[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/issue-ws-token?${params}`, {
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
| `publicId` | string | yes |  |
| `scopes[]` | array<string> | yes |  |
| `keys[]` | array<string> | yes |  |
| `expire` | number | no | Default: `60`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "wsToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Response status code |
| `wsToken` | string | Temporary WS token |

## Native endpoint

Through the native Cloud BOT API, this operation is `POST /:public_id/ws_tokens` (base URL `https://api.c-bot.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/issue-ws-token.md) for the provider-specific parameters and requirements.

