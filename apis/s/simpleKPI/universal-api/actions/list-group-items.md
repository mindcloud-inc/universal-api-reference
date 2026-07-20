# SimpleKPI: List Group Items

Retrieves group items from a SimpleKPI group.

```
GET https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-group-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SimpleKPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-group-items?connectionId=$CONNECTION_ID&groupId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-group-items?${params}`, {
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
| `groupId` | number | yes | SimpleKPI group ID. |

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

Through the native SimpleKPI API, this operation is `GET groups/:groupId/items` (base URL `https://{{credentials.subdomain}}.simplekpi.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-items.md) for the provider-specific parameters and requirements.

