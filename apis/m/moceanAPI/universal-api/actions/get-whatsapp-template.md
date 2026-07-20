# Mocean API: Get WhatsApp Template



```
GET https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/get-whatsapp-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/get-whatsapp-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/get-whatsapp-template?${params}`, {
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
| `templateId` | string | yes | The WhatsApp template ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "components": [
        {}
      ],
      "id": "string",
      "language": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `components` | array<object> |  |
| `id` | string |  |
| `language` | string |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Mocean API API, this operation is `GET /template/whatsapp/:templateId` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-whatsapp-template.md) for the provider-specific parameters and requirements.

