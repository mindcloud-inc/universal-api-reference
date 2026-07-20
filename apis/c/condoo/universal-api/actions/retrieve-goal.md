# condoo: Retrieve Goal

Retrieves a goal from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-goal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-goal?connectionId=$CONNECTION_ID&goalId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "goalId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/retrieve-goal?${params}`, {
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
| `goalId` | number | yes | Required goal ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datetime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "key": "string",
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "path": "string",
      "type": "string",
      "user_id": 1,
      "website_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datetime` | date |  |
| `id` | number |  |
| `key` | string |  |
| `last_datetime` | date |  |
| `name` | string |  |
| `path` | string |  |
| `type` | string |  |
| `user_id` | number |  |
| `website_id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `GET /goals/{goal_id}` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-goal.md) for the provider-specific parameters and requirements.

