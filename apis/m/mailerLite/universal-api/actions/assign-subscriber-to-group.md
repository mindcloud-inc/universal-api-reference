# MailerLite: Assign Subscriber to Group

Assigns an existing subscriber to a group in MailerLite.

```
PUT https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/assign-subscriber-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/assign-subscriber-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriber_id": "180863157267334516",
  "group_id": "180900000000000001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/assign-subscriber-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriber_id": "180863157267334516",
    "group_id": "180900000000000001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriber_id` | string | yes | Existing MailerLite subscriber identifier. Example: `180863157267334516`. |
| `group_id` | string | yes | Existing MailerLite group identifier. Example: `180900000000000001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeCount": 1,
      "bouncedCount": 1,
      "clickRate": {},
      "clicksCount": 1,
      "createdAt": "string",
      "id": "string",
      "junkCount": 1,
      "name": "Ava Chen",
      "openRate": {},
      "opensCount": 1,
      "sentCount": 1,
      "unconfirmedCount": 1,
      "unsubscribedCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeCount` | number |  |
| `bouncedCount` | number |  |
| `clickRate` | object |  |
| `clicksCount` | number |  |
| `createdAt` | string |  |
| `id` | string |  |
| `junkCount` | number |  |
| `name` | string |  |
| `openRate` | object |  |
| `opensCount` | number |  |
| `sentCount` | number |  |
| `unconfirmedCount` | number |  |
| `unsubscribedCount` | number |  |

## Native endpoint

Through the native MailerLite API, this operation is `POST /subscribers/:subscriber_id/groups/:group_id` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-subscriber-to-group.md) for the provider-specific parameters and requirements.

