# EventGeek: Get Field

Retrieves a custom field from EventGeek by ID.

```
GET https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-field?connectionId=$CONNECTION_ID&field_id=Q3VzdG9tRmllbGRUeXBlLTE5NjkwOA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "field_id": "Q3VzdG9tRmllbGRUeXBlLTE5NjkwOA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/get-field?${params}`, {
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
| `field_id` | string | yes | Circa field identifier. Default: `Q3VzdG9tRmllbGRUeXBlLTE5NjkwOA`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_for": "string",
      "field_type": "string",
      "id": "string",
      "label": "string",
      "name": "Ava Chen",
      "options": [
        "string"
      ],
      "required": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field_for` | string |  |
| `field_type` | string |  |
| `id` | string |  |
| `label` | string |  |
| `name` | string |  |
| `options` | array<string> |  |
| `required` | boolean |  |

## Native endpoint

Through the native EventGeek API, this operation is `GET /fields/:field_id` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-field.md) for the provider-specific parameters and requirements.

