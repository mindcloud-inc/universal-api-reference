# LLMWhisperer: Retrieve Extracted Text

Retrieves extracted text from an LLMWhisperer extraction job.

```
GET https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/retrieve-extracted-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMWhisperer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/retrieve-extracted-text?connectionId=$CONNECTION_ID&whisperHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "whisperHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMWhisperer/latest/actions/retrieve-extracted-text?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `text` | string |  |

## Native endpoint

Through the native LLMWhisperer API, this operation is `GET /whisper-retrieve` (base URL `https://llmwhisperer-api.us-central.unstract.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-extracted-text.md) for the provider-specific parameters and requirements.

