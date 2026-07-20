# elmah.io: Delete Messages

Deletes messages from a log in elmah.io.

```
DELETE https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/delete-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a elmah.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/delete-messages?connectionId=$CONNECTION_ID&logId=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "logId": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/delete-messages?${params}`, {
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
| `logId` | string | yes | The ID of the log containing the messages. |
| `query` | string | yes | Lucene query. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native elmah.io API returns.

## Native endpoint

Through the native elmah.io API, this operation is `DELETE /v3/messages/:logId` (base URL `https://api.elmah.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-messages.md) for the provider-specific parameters and requirements.

