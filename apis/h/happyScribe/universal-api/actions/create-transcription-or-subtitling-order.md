# HappyScribe: Create Transcription or Subtitling Order

Creates a transcription or subtitling order in HappyScribe.

```
POST https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/create-transcription-or-subtitling-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/create-transcription-or-subtitling-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language": "en-US",
  "url": "https://example.com/media.mp3"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/create-transcription-or-subtitling-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "language": "en-US",
    "url": "https://example.com/media.mp3"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `confirm` | boolean | no | When true, submit the order immediately if there are no errors. Default: `false`. |
| `language` | string | yes | Language code of the source media. Example: `en-US`. |
| `service` | string | no | Service type: auto for machine transcription or pro for human transcription. Default: `auto`. Example: `auto`. |
| `url` | string | yes | Publicly accessible media URL to ingest for transcription or subtitling. Example: `https://example.com/media.mp3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canBeSubmitted": true,
      "details": {},
      "folder_id": 1,
      "id": "string",
      "ingestions": [
        {}
      ],
      "inputs": [
        {}
      ],
      "operations": [
        {}
      ],
      "state": "string",
      "transcriptions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canBeSubmitted` | boolean |  |
| `details` | object |  |
| `folder_id` | number |  |
| `id` | string |  |
| `ingestions` | array<object> |  |
| `inputs` | array<object> |  |
| `operations` | array<object> |  |
| `state` | string |  |
| `transcriptions` | array<object> |  |

## Native endpoint

Through the native HappyScribe API, this operation is `POST /orders` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transcription-or-subtitling-order.md) for the provider-specific parameters and requirements.

