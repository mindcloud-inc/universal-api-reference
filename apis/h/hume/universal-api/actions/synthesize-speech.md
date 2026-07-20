# Hume: Synthesize speech



```
POST https://connect.mindcloud.co/v1/universal/hume/latest/actions/synthesize-speech
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hume `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hume/latest/actions/synthesize-speech" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "utterances[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hume/latest/actions/synthesize-speech', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "utterances[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `utterances[]` | array<object> | yes | Array of utterances to synthesize. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | object | no | Optional output audio format object, for example {"type":"mp3"}. |
| `splitUtterances` | boolean | no | Whether to split utterances into natural-sounding segments. Default: `true`. |
| `numGenerations` | number | no | Number of generations to produce. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generations": [
        [
          {}
        ]
      ],
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generations[]` | array<object> |  |
| `requestId` | string |  |

## Native endpoint

Through the native Hume API, this operation is `POST /v0/tts` (base URL `https://api.hume.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/synthesize-speech.md) for the provider-specific parameters and requirements.

