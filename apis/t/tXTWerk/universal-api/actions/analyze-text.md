# TXT Werk: Analyze Text

Analyzes text content in TXT Werk.

```
GET https://connect.mindcloud.co/v1/universal/tXTWerk/latest/actions/analyze-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TXT Werk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tXTWerk/latest/actions/analyze-text?connectionId=$CONNECTION_ID&text=string&services=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string",
  "services": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tXTWerk/latest/actions/analyze-text?${params}`, {
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
| `text` | string | yes | The text to analyze. |
| `services` | string | yes | Comma-separated analysis services to run. |
| `language` | string | no | Optional input language; omit to let TXT Werk detect it automatically. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {
          "confidence": 1,
          "label": "string"
        }
      ],
      "language": "string",
      "tags": [
        {
          "confidence": 1,
          "term": "string"
        }
      ],
      "text": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories[].confidence` | number |  |
| `categories[].label` | string |  |
| `language` | string |  |
| `tags[].confidence` | number |  |
| `tags[].term` | string |  |
| `text` | string |  |
| `timestamp` | number |  |

## Native endpoint

Through the native TXT Werk API, this operation is `POST /rest/txt/analyzer` (base URL `https://api.txtwerk.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-text.md) for the provider-specific parameters and requirements.

