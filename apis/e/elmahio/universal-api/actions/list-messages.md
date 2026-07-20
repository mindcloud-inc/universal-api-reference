# elmah.io: List Messages

Retrieves messages from a log in elmah.io.

```
GET https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a elmah.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/list-messages?connectionId=$CONNECTION_ID&logId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "logId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/list-messages?${params}`, {
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
| `from` | string | no | A start date and time to search from. |
| `includeHeaders` | boolean | no | Include headers like server variables and cookies in the result. |
| `logId` | string | yes | The ID of the log containing the messages. |
| `pageIndex` | number | no | The page number of the result. |
| `pageSize` | number | no | The number of messages to load, max 100. |
| `query` | string | no | A full-text or Lucene query to limit the messages by. |
| `searchAfter` | string | no | Continue from the end of the previous search result. |
| `to` | string | no | An end date and time to search to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messages": [
        {}
      ],
      "searchAfter": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messages` | array<object> |  |
| `searchAfter` | string |  |
| `total` | number |  |

## Native endpoint

Through the native elmah.io API, this operation is `GET /v3/messages/:logId` (base URL `https://api.elmah.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

