# Discourse: Silence User

Silences an existing user in Discourse.

```
PUT https://connect.mindcloud.co/v1/universal/discourse/latest/actions/silence-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/silence-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "silenced_till": "string",
  "reason": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/silence-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "silenced_till": "string",
    "reason": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | User id. |
| `post_action` | string | no | Optional moderation action to take on the user's posts. One of: `0`. |
| `silenced_till` | string | yes | Date/time until the user is silenced. |
| `reason` | string | yes | Silence reason. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | no | Optional message sent with the silence. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "silence": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `silence` | object |  |

## Native endpoint

Through the native Discourse API, this operation is `PUT /admin/users/:id/silence.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/silence-user.md) for the provider-specific parameters and requirements.

