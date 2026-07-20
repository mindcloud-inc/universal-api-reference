# Open Letter Connect: Create Template

Creates a template in Open Letter Connect.

```
POST https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Letter Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openLetterConnect/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[0].defaultValue` | string | no | The default value for the first template field. |
| `fields[0].key` | string | no | The merge field token for the first template field. |
| `fields[0].strict` | string | no | Whether the first template field is strict. |
| `fields[0].value` | string | no | The display label for the first template field. |
| `productId` | string | no | The product ID the template belongs to. |
| `templatePath` | string | no | The uploaded template path returned by the upload endpoint. |
| `thumbnailPath` | string | no | The uploaded thumbnail path returned by the upload endpoint. |
| `title` | string | no | The template title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creator": {
        "fullName": "Ava Chen",
        "id": "string"
      },
      "id": "string",
      "product": {
        "deliveryType": "string",
        "envelopeType": "string",
        "id": "string",
        "name": "Ava Chen",
        "paperSize": "string",
        "paperType": "string",
        "postageType": "string",
        "productType": "string"
      },
      "templateType": "string",
      "templateUrl": "https://example.com",
      "thumbnailUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creator.fullName` | string |  |
| `creator.id` | string |  |
| `id` | string |  |
| `product.deliveryType` | string |  |
| `product.envelopeType` | string |  |
| `product.id` | string |  |
| `product.name` | string |  |
| `product.paperSize` | string |  |
| `product.paperType` | string |  |
| `product.postageType` | string |  |
| `product.productType` | string |  |
| `templateType` | string |  |
| `templateUrl` | string |  |
| `thumbnailUrl` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Open Letter Connect API, this operation is `POST /templates` (base URL `https://api.openletterconnect.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

