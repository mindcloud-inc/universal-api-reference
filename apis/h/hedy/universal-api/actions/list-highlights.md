# Hedy: List Highlights

Retrieves highlight records from Hedy.

```
GET https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-highlights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-highlights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/list-highlights?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "highlightId": "string",
      "sessionId": "string",
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
| `highlightId` | string |  |
| `sessionId` | string |  |
| `timestamp` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Hedy API, this operation is `GET https://api.hedy.bot/highlights` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-highlights.md) for the provider-specific parameters and requirements.

