# Runrun.it: List Activities

Retrieves activities from Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/list-activities?${params}`, {
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
| `sort` | string | no | Sort by column |
| `sortDir` | string | no | Sort direction ('asc' or 'desc') |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actor_id": "string",
      "actor_name": "Ava Chen",
      "happened_at": "string",
      "id": 1,
      "key": "string",
      "message": "string",
      "trackable_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actor_id` | string |  |
| `actor_name` | string |  |
| `happened_at` | string |  |
| `id` | number |  |
| `key` | string |  |
| `message` | string |  |
| `trackable_type` | string |  |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /activities` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

