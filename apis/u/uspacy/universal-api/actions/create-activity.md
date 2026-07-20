# Uspacy: Create Activity

Creates a new activity in Uspacy.

```
POST https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uspacy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "start_time": 1,
  "end_time": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uspacy/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "start_time": 1,
    "end_time": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The activity title. |
| `start_time` | number | yes | The activity start timestamp. |
| `end_time` | number | yes | The activity end timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "end_time": 1,
      "id": 1,
      "priority": "string",
      "responsible_id": 1,
      "start_time": 1,
      "status": "string",
      "title": "string",
      "type": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `end_time` | number |  |
| `id` | number |  |
| `priority` | string |  |
| `responsible_id` | number |  |
| `start_time` | number |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native Uspacy API, this operation is `POST /activities/v1/activities` (base URL `https://{{credentials.site}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity.md) for the provider-specific parameters and requirements.

