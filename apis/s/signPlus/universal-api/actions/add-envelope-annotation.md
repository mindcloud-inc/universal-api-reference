# Sign.Plus: Add Envelope Annotation



```
POST https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/add-envelope-annotation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign.Plus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/add-envelope-annotation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "envelopeId": "string",
  "recipientId": "string",
  "documentId": "string",
  "page": 1,
  "x": 1,
  "y": 1,
  "width": 1,
  "height": 1,
  "required": true,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/add-envelope-annotation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "envelopeId": "string",
    "recipientId": "string",
    "documentId": "string",
    "page": 1,
    "x": 1,
    "y": 1,
    "width": 1,
    "height": 1,
    "required": true,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `envelopeId` | string | yes |  |
| `recipientId` | string | yes |  |
| `documentId` | string | yes |  |
| `page` | number | yes |  |
| `x` | number | yes |  |
| `y` | number | yes |  |
| `width` | number | yes |  |
| `height` | number | yes |  |
| `required` | boolean | yes |  |
| `type` | string | yes |  |
| `text` | object | no |  |
| `signature` | object | no | JSON object for SIGNATURE annotations, for example {"id":""} |
| `initials` | object | no | JSON object for INITIALS annotations |
| `datetime` | object | no | JSON object for DATETIME annotations |
| `checkbox` | object | no | JSON object for CHECKBOX annotations |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkbox": {},
      "datetime": {},
      "document_id": "string",
      "height": 1,
      "id": "string",
      "initials": {},
      "page": 1,
      "recipient_id": "string",
      "required": true,
      "signature": {},
      "text": {},
      "type": "string",
      "width": 1,
      "x": 1,
      "y": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkbox` | object |  |
| `datetime` | object |  |
| `document_id` | string |  |
| `height` | number |  |
| `id` | string |  |
| `initials` | object |  |
| `page` | number |  |
| `recipient_id` | string |  |
| `required` | boolean |  |
| `signature` | object |  |
| `text` | object |  |
| `type` | string |  |
| `width` | number |  |
| `x` | number |  |
| `y` | number |  |

## Native endpoint

Through the native Sign.Plus API, this operation is `POST /envelope/:envelope_id/annotation` (base URL `https://restapi.sign.plus/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-envelope-annotation.md) for the provider-specific parameters and requirements.

