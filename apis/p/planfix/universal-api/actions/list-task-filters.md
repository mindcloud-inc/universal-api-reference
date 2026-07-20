# Planfix: List Task Filters

Retrieves task filters from Planfix.

```
GET https://connect.mindcloud.co/v1/universal/planfix/latest/actions/list-task-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planfix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planfix/latest/actions/list-task-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planfix/latest/actions/list-task-filters?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Planfix API, this operation is `POST /task/filters` (base URL `{{credentials.accountBaseUrl}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-filters.md) for the provider-specific parameters and requirements.

