# mintBlue: Update Project

Updates an existing project in mintBlue.

```
PUT https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mintBlue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params.id": "string",
  "params.data.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mintBlue/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params.id": "string",
    "params.data.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params.id` | string | yes | Project ID to update. |
| `params.data.name` | string | yes | Project name. |
| `params.data.description` | string | no | Optional project description. |
| `params.data.tags[]` | array<string> | no | Optional project tags. |

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

Through the native mintBlue API, this operation is `POST /sdk/latest` (base URL `https://api.mintblue.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

