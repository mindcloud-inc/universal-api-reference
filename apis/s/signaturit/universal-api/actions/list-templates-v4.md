# Signaturit: List Templates V4

Retrieves templates from Signaturit V4 API.

```
GET https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-templates-v4
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Signaturit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-templates-v4?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signaturit/latest/actions/list-templates-v4?${params}`, {
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
| `limit` | number | no | Max number of templates to retrieve. Default: `10`. Example: `10`. |
| `page` | number | no | Results page number. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": "string",
      "name": "Ava Chen",
      "widgets": [
        {
          "created_at": "string",
          "default_value": "string",
          "editable": true,
          "id": "string",
          "key": "string",
          "left": 1,
          "name": "Ava Chen",
          "page": 1,
          "required": true,
          "top": 1,
          "type": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | string |  |
| `name` | string |  |
| `widgets[].created_at` | string |  |
| `widgets[].default_value` | string |  |
| `widgets[].editable` | boolean |  |
| `widgets[].id` | string |  |
| `widgets[].key` | string |  |
| `widgets[].left` | number |  |
| `widgets[].name` | string |  |
| `widgets[].page` | number |  |
| `widgets[].required` | boolean |  |
| `widgets[].top` | number |  |
| `widgets[].type` | string |  |

## Native endpoint

Through the native Signaturit API, this operation is `GET https://api.sandbox.signaturit.com/v4/templates` (base URL `https://api.sandbox.signaturit.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates-v4.md) for the provider-specific parameters and requirements.

