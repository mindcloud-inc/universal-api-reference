# ActiveTrail: Add Contact to Group

Adds a contact to a group in ActiveTrail.

```
POST https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/add-contact-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ActiveTrail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/add-contact-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/activeTrail/latest/actions/add-contact-to-group', {
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
| `doubleOptin` | string | no | Double opt-in settings. |
| `email` | string | no | Required if SMS is null. |
| `firstName` | string | no | Contact field. |
| `id` | number | yes | Group id. Can be found using the account groups endpoint or in the UI. |
| `lastName` | string | no | Contact field. |
| `sms` | string | no | Required if email is null. |
| `smsStatus` | string | no | Choose the SMS status. |
| `status` | string | no | Choose the contact status. |
| `subscribeIp` | string | no | The subscribe IP. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ActiveTrail API returns.

## Native endpoint

Through the native ActiveTrail API, this operation is `POST /groups/:id/members` (base URL `https://webapi.mymarketing.co.il/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-to-group.md) for the provider-specific parameters and requirements.

