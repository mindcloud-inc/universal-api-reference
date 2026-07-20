# HappyFox: List Ticket Custom Fields

Retrieves ticket custom fields from HappyFox.

```
GET https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-ticket-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HappyFox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-ticket-custom-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/happyFox/latest/actions/list-ticket-custom-fields?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        {}
      ],
      "choices": [
        {}
      ],
      "compulsoryOnCompleted": true,
      "compulsoryOnMove": true,
      "dependsOnChoice": 1,
      "id": 1,
      "name": "Ava Chen",
      "order": 1,
      "required": true,
      "type": "string",
      "visibleToStaffOnly": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> | Ticket categories where the field is available. |
| `choices` | array<object> | Available field choices. |
| `compulsoryOnCompleted` | boolean | Whether the field is required when the ticket is completed. |
| `compulsoryOnMove` | boolean | Whether the field is required when the ticket is moved. |
| `dependsOnChoice` | number | Choice ID this field depends on, when configured. |
| `id` | number | HappyFox ticket custom field ID. |
| `name` | string | Ticket custom field label. |
| `order` | number | Sort order of the custom field. |
| `required` | boolean | Whether the custom field is required. |
| `type` | string | HappyFox custom field type. |
| `visibleToStaffOnly` | boolean | Whether the custom field is only visible to staff. |

## Native endpoint

Through the native HappyFox API, this operation is `GET /ticket_custom_fields/` (base URL `https://{{credentials.accountDomain}}/api/1.1/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-custom-fields.md) for the provider-specific parameters and requirements.

