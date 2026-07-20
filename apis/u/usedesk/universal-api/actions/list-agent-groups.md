# Usedesk: List Agent Groups

Retrieves a list of agent groups from Usedesk.

```
GET https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-agent-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-agent-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-agent-groups?${params}`, {
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
      "company_id": 1,
      "custom_working_time": 1,
      "deleted": 1,
      "deleted_at": "string",
      "id": 1,
      "name": "Ava Chen",
      "timezone": "string",
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | number |  |
| `custom_working_time` | number |  |
| `deleted` | number |  |
| `deleted_at` | string |  |
| `id` | number |  |
| `name` | string |  |
| `timezone` | string |  |
| `users` | array<object> |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /groups` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agent-groups.md) for the provider-specific parameters and requirements.

