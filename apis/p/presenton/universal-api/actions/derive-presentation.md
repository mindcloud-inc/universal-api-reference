# Presenton: Derive Presentation



```
POST https://connect.mindcloud.co/v1/universal/presenton/latest/actions/derive-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/derive-presentation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "presentationId": "string",
  "slides[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/presenton/latest/actions/derive-presentation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "presentationId": "string",
    "slides[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `presentationId` | string | yes | The source presentation ID. |
| `slides[]` | array<object> | yes | Slides array with updates for the derived deck. |
| `exportAs` | string | no | Export format such as pptx or pdf. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "editPath": "string",
      "path": "string",
      "presentationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number |  |
| `editPath` | string |  |
| `path` | string |  |
| `presentationId` | string |  |

## Native endpoint

Through the native Presenton API, this operation is `POST /api/v1/ppt/presentation/derive` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/derive-presentation.md) for the provider-specific parameters and requirements.

