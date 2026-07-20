# AI21 Labs: Extract Keywords

Creates a keyword extraction run in AI21 Labs.

```
POST https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/extract-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AI21 Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/extract-keywords" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "Paste the text to analyze for keywords and phrases."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aI21Labs/latest/actions/extract-keywords', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "Paste the text to analyze for keywords and phrases."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | The text to extract important keywords and phrases from. Example: `Paste the text to analyze for keywords and phrases.`. |
| `budget` | string | no | AI21 reasoning budget such as low, medium, or high. One of: `0`, `1`, `2`. Default: `low`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data_sources": [
        {}
      ],
      "error": {},
      "id": "string",
      "requirements_result": {},
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data_sources` | array<object> | Data sources used by the run when AI21 provides them. |
| `error` | object | Error details when the run fails. |
| `id` | string | The AI21 Maestro run id. |
| `requirements_result` | object | Structured requirement-evaluation output when the prompt asks for it. |
| `result` | string | The final generated output when the run completes. |
| `status` | string | The current lifecycle status of the run. |

## Native endpoint

Through the native AI21 Labs API, this operation is `POST /maestro/runs` (base URL `https://api.ai21.com/studio/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-keywords.md) for the provider-specific parameters and requirements.

