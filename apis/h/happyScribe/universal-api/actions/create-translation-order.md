# HappyScribe: Create Translation Order

Creates a translation order in HappyScribe.

```
POST https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/create-translation-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyScribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/create-translation-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceTranscriptionId": "string",
  "targetLanguages[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/happyScribe/latest/actions/create-translation-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceTranscriptionId": "string",
    "targetLanguages[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `confirm` | boolean | no | When true, submit the translation order immediately if there are no errors. Default: `false`. |
| `service` | string | no | Service type: auto or pro. Default: `auto`. Example: `auto`. |
| `sourceTranscriptionId` | string | yes | Source transcription to translate. |
| `targetLanguages[]` | array<string> | yes | One or more target language codes. |

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

Through the native HappyScribe API, this operation is `POST /orders/translation` (base URL `https://www.happyscribe.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-translation-order.md) for the provider-specific parameters and requirements.

