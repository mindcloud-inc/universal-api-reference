# Tiliter: Create Recognition Request

Creates a recognition request in the Tiliter Recognition API.

```
POST https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-recognition-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-recognition-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deviceId": "string",
  "images[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/create-recognition-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deviceId": "string",
    "images[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceId` | string | yes |  |
| `images[]` | array<object> | yes |  |
| `weightGrams` | number | no |  |
| `includeScores` | boolean | no |  |
| `maxOptions` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bagRecognition": {
        "present": true,
        "type": "string"
      },
      "id": "string",
      "productRecognition": {
        "options": [
          {
            "productId": "string",
            "score": 1
          }
        ],
        "resultType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bagRecognition` | object |  |
| `bagRecognition.present` | boolean |  |
| `bagRecognition.type` | string |  |
| `id` | string |  |
| `productRecognition` | object |  |
| `productRecognition.options` | array<object> |  |
| `productRecognition.options[].productId` | string |  |
| `productRecognition.options[].score` | number |  |
| `productRecognition.resultType` | string |  |

## Native endpoint

Through the native Tiliter API, this operation is `POST /recognition/` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recognition-request.md) for the provider-specific parameters and requirements.

