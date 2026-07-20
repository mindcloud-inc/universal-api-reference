# LLMWhisperer: Get Highlight Lines

Retrieves highlight line metadata from an LLMWhisperer extraction job.

```
GET https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-highlight-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMWhisperer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-highlight-lines?connectionId=$CONNECTION_ID&whisperHash=string&lines=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "whisperHash": "string",
  "lines": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/get-highlight-lines?${params}`, {
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
| `whisperHash` | string | yes | Extraction job hash returned by the extraction API. |
| `lines` | string | yes | Line range selector such as 1-10. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LLMWhisperer API returns.

## Native endpoint

Through the native LLMWhisperer API, this operation is `GET /highlights` (base URL `https://llmwhisperer-api.us-central.unstract.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-highlight-lines.md) for the provider-specific parameters and requirements.

