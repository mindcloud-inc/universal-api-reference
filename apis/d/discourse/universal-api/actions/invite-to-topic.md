# Discourse: Invite To Topic

Invites a user to a Discourse topic.

```
POST https://connect.mindcloud.co/v1/universal/discourse/latest/actions/invite-to-topic
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discourse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/invite-to-topic" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/invite-to-topic', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Email address to invite to the topic. |
| `id` | number | yes | Topic id. |
| `user` | string | no | Username to invite to the topic. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user` | object |  |

## Native endpoint

Through the native Discourse API, this operation is `POST /t/:id/invite.json` (base URL `https://mindcloud.discourse.group`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/invite-to-topic.md) for the provider-specific parameters and requirements.

