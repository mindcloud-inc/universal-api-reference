# Are.na: Create Connection

Creates a new connection in Are.na.

```
POST https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Are.na `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-connection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel_ids[]": [
    1
  ],
  "connectable_id": 1,
  "connectable_type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/are-na/latest/actions/create-connection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel_ids[]": [1],
    "connectable_id": 1,
    "connectable_type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel_ids[]` | array<number> | yes | Array of channel IDs to connect the item into. |
| `connectable_id` | number | yes | ID of the block or channel to connect. |
| `connectable_type` | string | yes | Type of item to connect: Block or Channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": {},
      "connectable": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | object |  |
| `connectable` | object |  |
| `created_at` | date |  |
| `id` | number |  |
| `position` | number |  |

## Native endpoint

Through the native Are.na API, this operation is `POST connections` (base URL `https://api.are.na/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-connection.md) for the provider-specific parameters and requirements.

