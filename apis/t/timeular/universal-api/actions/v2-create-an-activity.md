# Timeular: V2 Create an Activity

Creates a new activity in the Timeular v2 API.

```
POST https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-create-an-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-create-an-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-create-an-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | string | no |  |
| `integration` | string | no |  |
| `name` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "deviceSide": "string",
      "id": "string",
      "integration": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `deviceSide` | string |  |
| `id` | string |  |
| `integration` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v2/activities` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-create-an-activity.md) for the provider-specific parameters and requirements.

