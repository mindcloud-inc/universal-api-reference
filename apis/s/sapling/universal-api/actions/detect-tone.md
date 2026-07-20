# Sapling: Detect Tone

Detects tone in text with Sapling.

```
GET https://connect.mindcloud.co/v1/universal/sapling/latest/actions/detect-tone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/detect-tone?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sapling/latest/actions/detect-tone?${params}`, {
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
| `text` | string | yes | Text to analyze the tone for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "overall": [
        {}
      ],
      "results": [
        {}
      ],
      "sents": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `overall` | array<object> | Overall tone classification. |
| `results` | array<object> | Per-span tone analysis. |
| `sents` | array<string> | Normalized sentence list. |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/tone` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-tone.md) for the provider-specific parameters and requirements.

