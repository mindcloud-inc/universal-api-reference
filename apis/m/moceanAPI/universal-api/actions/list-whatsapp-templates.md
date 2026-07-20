# Mocean API: List WhatsApp Templates



```
GET https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/list-whatsapp-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/list-whatsapp-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/list-whatsapp-templates?${params}`, {
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
| `category` | string | no | Optional template category filter. |
| `language` | string | no | Optional template language filter. |
| `limit` | string | no | Maximum number of templates to return. |
| `name` | string | no | Optional template name filter. |
| `status` | string | no | Optional template review status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "category": "string",
          "id": "string",
          "language": "string",
          "name": "Ava Chen",
          "status": "string"
        }
      ],
      "paging": {
        "cursors": {
          "after": "string",
          "before": "string"
        },
        "next": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].category` | string |  |
| `data[].id` | string |  |
| `data[].language` | string |  |
| `data[].name` | string |  |
| `data[].status` | string |  |
| `paging` | object |  |
| `paging.cursors` | object |  |
| `paging.cursors.after` | string |  |
| `paging.cursors.before` | string |  |
| `paging.next` | string |  |

## Native endpoint

Through the native Mocean API API, this operation is `GET /template/whatsapp/message_templates` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-whatsapp-templates.md) for the provider-specific parameters and requirements.

