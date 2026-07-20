# mintBlue: List Projects

Retrieves projects from mintBlue.

```
GET https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mintBlue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/list-projects?${params}`, {
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
      "archived_at": "string",
      "avg_transactions_size": 1,
      "created_at": "string",
      "default_key_id": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "tags": [
        "string"
      ],
      "total_transactions_count": 1,
      "total_transactions_size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_at` | string |  |
| `avg_transactions_size` | number |  |
| `created_at` | string |  |
| `default_key_id` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `tags` | array<string> |  |
| `total_transactions_count` | number |  |
| `total_transactions_size` | number |  |

## Native endpoint

Through the native mintBlue API, this operation is `POST /sdk/latest` (base URL `https://api.mintblue.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

