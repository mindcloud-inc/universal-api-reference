# SimpleKPI: Update Group Item

Updates an existing group item in SimpleKPI.

```
PUT https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/update-group-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/update-group-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/update-group-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | number | no | The group ID. |
| `id` | number | no | The group item ID. |
| `name` | string | no | The group item name. |
| `sort_order` | number | no | The display sort order of the group item. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "group_id": 1,
      "id": 1,
      "name": "Ava Chen",
      "sort_order": 1,
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
| `group_id` | number |  |
| `id` | number |  |
| `name` | string |  |
| `sort_order` | number |  |
| `updated_at` | string |  |

## Native endpoint

Through the native SimpleKPI API, this operation is `PUT groups/:groupId/items/:id` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group-item.md) for the provider-specific parameters and requirements.

