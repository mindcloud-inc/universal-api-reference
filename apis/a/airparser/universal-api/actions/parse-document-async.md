# Airparser: Parse Document Async

Parses a document asynchronously in Airparser.

```
POST https://connect.mindcloud.co/v1/universal/airparser/latest/actions/parse-document-async
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airparser/latest/actions/parse-document-async" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": "string",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airparser/latest/actions/parse-document-async', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": "string",
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxId` | string | yes | The Airparser inbox ID. |
| `file` | file | yes | The file to upload for parsing. |
| `meta` | string | no | Optional JSON string included in the parsed output as meta. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airparser API returns.

## Native endpoint

Through the native Airparser API, this operation is `POST /inboxes/:inbox_id/upload` (base URL `https://api.airparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-document-async.md) for the provider-specific parameters and requirements.

