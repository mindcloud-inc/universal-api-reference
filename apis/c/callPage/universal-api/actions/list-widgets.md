# CallPage: List Widgets

Retrieves all available widgets from CallPage.

```
GET https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-widgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-widgets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callPage/latest/actions/list-widgets?${params}`, {
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
      "assignments": [
        {}
      ],
      "call_requests_count": 1,
      "company_sms_name": "Ava Chen",
      "description": "string",
      "enabled": true,
      "id": 1,
      "installation_status": 1,
      "installed_at": "string",
      "locale_code": "string",
      "url": "https://example.com",
      "widget_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignments` | array<object> |  |
| `call_requests_count` | number |  |
| `company_sms_name` | string |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `id` | number |  |
| `installation_status` | number |  |
| `installed_at` | string |  |
| `locale_code` | string |  |
| `url` | string |  |
| `widget_code` | string |  |

## Native endpoint

Through the native CallPage API, this operation is `GET /widgets/all` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-widgets.md) for the provider-specific parameters and requirements.

