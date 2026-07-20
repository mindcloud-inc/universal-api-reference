# Hedy: List Session Highlights

Retrieves highlights for a Hedy session.

```
GET https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-session-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-session-highlights?connectionId=$CONNECTION_ID&sessionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-session-highlights?${params}`, {
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
| `format` | string | no | Set to zapier to receive a flat array response suitable for Zapier triggers. |
| `sessionId` | string | yes | Unique identifier of the session. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiInsight": "string",
      "cleanedQuote": "string",
      "id": "string",
      "mainIdea": "string",
      "rawQuote": "string",
      "sessionId": "string",
      "timeIndex": 1,
      "timestamp": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aiInsight` | string |  |
| `cleanedQuote` | string |  |
| `id` | string |  |
| `mainIdea` | string |  |
| `rawQuote` | string |  |
| `sessionId` | string |  |
| `timeIndex` | number |  |
| `timestamp` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Hedy API, this operation is `GET https://api.hedy.bot/sessions/:sessionId/highlights` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-session-highlights.md) for the provider-specific parameters and requirements.

