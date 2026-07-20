# condoo: Create Goal

Creates a new goal in condoo.

```
POST https://connect.mindcloud.co/v1/universal/condoo/latest/actions/create-goal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/create-goal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string",
  "websiteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/condoo/latest/actions/create-goal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string",
    "websiteId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `key` | string | no | Optional custom goal key. |
| `name` | string | yes | Required goal name. |
| `path` | string | no | Optional path when type is pageview. |
| `type` | string | yes | Required goal type. Allowed values: pageview, custom. |
| `websiteId` | number | yes | Required website ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `POST /goals` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-goal.md) for the provider-specific parameters and requirements.

