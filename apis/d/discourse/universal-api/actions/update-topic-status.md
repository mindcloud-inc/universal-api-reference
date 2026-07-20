# Discourse: Update Topic Status

Updates a topic's status in Discourse.

```
PUT https://connect.mindcloud.co/v1/universal/discourse/latest/actions/update-topic-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/update-topic-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "status": "0",
  "enabled": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/update-topic-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "status": "0",
    "enabled": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Topic id. |
| `status` | string | yes | Topic status to change. One of: `0`, `1`, `2`, `3`, `4`. |
| `enabled` | string | yes | Set true to enable the status or false to disable it. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": "string",
      "topic_status_update": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | string |  |
| `topic_status_update` | object |  |

## Native endpoint

Through the native Discourse API, this operation is `PUT /t/:id/status.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-topic-status.md) for the provider-specific parameters and requirements.

