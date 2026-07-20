# Hedy: Get Highlight Details

Retrieves a highlight from Hedy.

```
GET https://connect.mindcloud.co/v1/universal/hedy/latest/actions/get-highlight-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/get-highlight-details?connectionId=$CONNECTION_ID&highlightId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "highlightId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/get-highlight-details?${params}`, {
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
| `highlightId` | string | yes | Unique identifier of the highlight. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiInsight": "string",
      "cleanedQuote": "string",
      "highlightId": "string",
      "mainIdea": "string",
      "rawQuote": "string",
      "sessionId": "string",
      "timeIndex": 1,
      "timestamp": "2026-05-07T12:00:00.000Z",
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
| `highlightId` | string |  |
| `mainIdea` | string |  |
| `rawQuote` | string |  |
| `sessionId` | string |  |
| `timeIndex` | number |  |
| `timestamp` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Hedy API, this operation is `GET https://api.hedy.bot/highlights/:highlightId` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-highlight-details.md) for the provider-specific parameters and requirements.

