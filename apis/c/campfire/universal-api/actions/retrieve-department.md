# Campfire: Retrieve Department

Retrieves a department from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-department
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-department?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-department?${params}`, {
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
| `id` | number | yes | The department ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "customer": 1,
      "display_name": "Ava Chen",
      "id": 1,
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "parent": 1,
      "parent_name": "Ava Chen",
      "tags": [
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
| `active` | boolean |  |
| `code` | string |  |
| `created_at` | date |  |
| `customer` | number |  |
| `display_name` | string |  |
| `id` | number |  |
| `last_modified_at` | date |  |
| `name` | string |  |
| `parent` | number |  |
| `parent_name` | string |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/department/:id` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-department.md) for the provider-specific parameters and requirements.

