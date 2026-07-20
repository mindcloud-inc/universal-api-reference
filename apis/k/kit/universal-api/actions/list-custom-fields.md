# Kit: List Custom Fields

Lists custom fields in your Kit account.

```
GET https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-custom-fields?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kit/latest/actions/list-custom-fields?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeTotalCount` | boolean | no | Set to true to include total_count in the response. Kit notes this can make the request slower. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_fields": [
        {
          "id": 1,
          "key": "string",
          "label": "string",
          "name": "Ava Chen"
        }
      ],
      "pagination": {
        "end_cursor": "string",
        "has_next_page": true,
        "has_previous_page": true,
        "per_page": 1,
        "start_cursor": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_fields` | array<object> | Collection of custom field objects. |
| `custom_fields[].id` | number | Custom field ID. |
| `custom_fields[].key` | string | Custom field key used in subscriber field payloads. |
| `custom_fields[].label` | string | Human-readable custom field label. |
| `custom_fields[].name` | string | Generated custom field name. |
| `pagination` | object | Cursor pagination metadata. |
| `pagination.end_cursor` | string | Cursor for requesting the next page. |
| `pagination.has_next_page` | boolean | Whether a next page is available. |
| `pagination.has_previous_page` | boolean | Whether a previous page is available. |
| `pagination.per_page` | number | Returned page size. |
| `pagination.start_cursor` | string | Cursor for requesting the previous page. |

## Native endpoint

Through the native Kit API, this operation is `GET /custom_fields` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-custom-fields.md) for the provider-specific parameters and requirements.

