# Runrun.it: Get Task Type

Retrieves a task type from Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-task-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-task-type?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-task-type?${params}`, {
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
| `id` | string | yes | Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avg_delivery": 1,
      "color": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_default": true,
      "is_public": true,
      "is_visible": true,
      "name": "Ava Chen",
      "standard_effort": "string",
      "standard_effort_time": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_delivery` | number | Average delivery time (in hours) to complete tasks of this type |
| `color` | string | Color of the type in hexadecimal format |
| `created_at` | date | Datetime of creation |
| `id` | number | Id of the type |
| `is_default` | boolean | True if is a system type |
| `is_public` | boolean | True if type is public |
| `is_visible` | boolean | Is the type visible to be chosen? (default: true) |
| `name` | string | Type name |
| `standard_effort` | string | Default effort to complete a task of this type (default: '00:00') |
| `standard_effort_time` | number | Default effort (in seconds) to complete a task of this type |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /task_types/:id` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-type.md) for the provider-specific parameters and requirements.

