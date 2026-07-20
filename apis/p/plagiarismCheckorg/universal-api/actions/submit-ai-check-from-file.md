# PlagiarismCheck.org: Submit AI Check From File



```
POST https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-ai-check-from-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PlagiarismCheck.org `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-ai-check-from-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plagiarismCheckorg/latest/actions/submit-ai-check-from-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | File to scan with the TraceGPT AI detector. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PlagiarismCheck.org API returns.

## Native endpoint

Through the native PlagiarismCheck.org API, this operation is `POST /api/v1/chat-gpt/` (base URL `https://plagiarismcheck.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-ai-check-from-file.md) for the provider-specific parameters and requirements.

