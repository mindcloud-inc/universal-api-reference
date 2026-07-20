# Discourse: Create Badge

Creates a new badge in Discourse.

```
POST https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-badge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-badge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "badge_type_id": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/create-badge', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "badge_type_id": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Badge name. |
| `badge_type_id` | number | yes | Badge type id: 1 gold, 2 silver, 3 bronze. One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "badge": {},
      "badge_types": [
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
| `badge` | object |  |
| `badge_types` | array<object> |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /admin/badges.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-badge.md) for the provider-specific parameters and requirements.

