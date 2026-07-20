# Sapling: Summarize Text

Summarizes input text into shorter output with Sapling.

```
GET https://connect.mindcloud.co/v1/universal/sapling/latest/actions/summarize-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/summarize-text?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/summarize-text?${params}`, {
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
| `text` | string | yes | Input document to summarize. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Summary text. |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/summarize` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/summarize-text.md) for the provider-specific parameters and requirements.

