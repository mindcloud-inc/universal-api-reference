# Presenton: Create Presentation From JSON Async



```
POST https://connect.mindcloud.co/v1/universal/presenton/latest/actions/create-presentation-from-json-async
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/create-presentation-from-json-async" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slides[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/presenton/latest/actions/create-presentation-from-json-async', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slides[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Presentation title. |
| `template` | string | no | Template ID such as general. |
| `slides[]` | array<object> | yes | Slides array matching the template layouts. |
| `exportAs` | string | no | Export format such as pptx or pdf. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "message": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `message` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Presenton API, this operation is `POST /api/v1/ppt/presentation/create/from-json/async` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-presentation-from-json-async.md) for the provider-specific parameters and requirements.

