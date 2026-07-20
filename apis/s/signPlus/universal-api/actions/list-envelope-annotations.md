# Sign.Plus: List Envelope Annotations



```
GET https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelope-annotations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sign.Plus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelope-annotations?connectionId=$CONNECTION_ID&envelopeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "envelopeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signPlus/latest/actions/list-envelope-annotations?${params}`, {
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
| `envelopeId` | string | yes |  |

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

Through the native Sign.Plus API, this operation is `GET /envelope/:envelope_id/annotations` (base URL `https://restapi.sign.plus/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-envelope-annotations.md) for the provider-specific parameters and requirements.

