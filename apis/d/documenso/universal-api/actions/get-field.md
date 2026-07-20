# Documenso: Get Field

Retrieves a field from Documenso.

```
GET https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documenso `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-field?connectionId=$CONNECTION_ID&fieldId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documenso/latest/actions/get-field?${params}`, {
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
| `fieldId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "envelopeId": "string",
      "envelopeItemId": "string",
      "fieldMeta": {},
      "height": "string",
      "id": 1,
      "inserted": true,
      "page": 1,
      "positionX": "string",
      "positionY": "string",
      "recipientId": 1,
      "secondaryId": "string",
      "type": "string",
      "width": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `envelopeId` | string |  |
| `envelopeItemId` | string |  |
| `fieldMeta` | object |  |
| `height` | string |  |
| `id` | number |  |
| `inserted` | boolean |  |
| `page` | number |  |
| `positionX` | string |  |
| `positionY` | string |  |
| `recipientId` | number |  |
| `secondaryId` | string |  |
| `type` | string |  |
| `width` | string |  |

## Native endpoint

Through the native Documenso API, this operation is `GET /envelope/field/:fieldId` (base URL `https://app.documenso.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-field.md) for the provider-specific parameters and requirements.

