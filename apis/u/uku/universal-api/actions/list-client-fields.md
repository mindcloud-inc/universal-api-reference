# Uku: List Client Fields

Retrieves client fields from Uku.

```
GET https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-client-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uku `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-client-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-client-fields?${params}`, {
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
      "created_at": "string",
      "data_column": "string",
      "default_title": "string",
      "group_name": "Ava Chen",
      "id": 1,
      "is_listed": 1,
      "is_visible": 1,
      "name": "Ava Chen",
      "required": 1,
      "sort_order": 1,
      "title": "string",
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `data_column` | string |  |
| `default_title` | string |  |
| `group_name` | string |  |
| `id` | number |  |
| `is_listed` | number |  |
| `is_visible` | number |  |
| `name` | string |  |
| `required` | number |  |
| `sort_order` | number |  |
| `title` | string |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uku API, this operation is `GET /client_fields` (base URL `https://app.getuku.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-client-fields.md) for the provider-specific parameters and requirements.

