# Oneflow: Get Template Type

Retrieves template type details from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-template-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-template-type?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/get-template-type?${params}`, {
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
| `id` | string | yes | The Oneflow template type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "active": true,
      "created_time": "string",
      "data_fields": [
        {}
      ],
      "description": "string",
      "extension_type": "string",
      "id": 1,
      "name": "Ava Chen",
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `active` | boolean |  |
| `created_time` | string |  |
| `data_fields` | array<object> |  |
| `description` | string |  |
| `extension_type` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updated_time` | string |  |

## Native endpoint

Through the native Oneflow API, this operation is `GET /template_types/:id` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-type.md) for the provider-specific parameters and requirements.

