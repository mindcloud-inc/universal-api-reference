# EventGeek: List Fields

Retrieves custom field records from EventGeek.

```
GET https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-fields?connectionId=$CONNECTION_ID&fields_for=Event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fields_for": "Event"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-fields?${params}`, {
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
| `fields_for` | string | yes | Object type to list fields for: Event, Company, or Contact. Default: `Event`. |

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

Through the native EventGeek API, this operation is `GET /fields` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

