# LogMeIn: Get Session Mailto Link

Retrieves a session email invitation link from LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-session-mailto-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-session-mailto-link?connectionId=$CONNECTION_ID&sessionId=string&language=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string",
  "language": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/get-session-mailto-link?${params}`, {
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
| `sessionId` | string | yes | Required session ID to generate the mailto invite link for. |
| `language` | string | yes | Required language code for the mailto link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": "https://example.com",
      "mailtoLink": "https://example.com",
      "sessionId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string |  |
| `mailtoLink` | string |  |
| `sessionId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `GET /goto-resolve/v1/sessions/:sessionId/invite/email` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-session-mailto-link.md) for the provider-specific parameters and requirements.

