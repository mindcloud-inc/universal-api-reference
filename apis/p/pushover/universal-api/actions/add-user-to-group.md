# Pushover: Add User to Group



```
POST https://connect.mindcloud.co/v1/universal/pushover/latest/actions/add-user-to-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/add-user-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group": "string",
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pushover/latest/actions/add-user-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group": "string",
    "user": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group` | string | yes | Delivery group key identifying which group to modify. |
| `user` | string | yes | Pushover user key to add to the group. |
| `device` | string | no | Optional device name to restrict notifications for this group member. |
| `memo` | string | no | Optional free-text memo associated with the group user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "request": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `request` | string | Pushover request identifier. |
| `status` | number | API status. Returns 1 when the group-user add request succeeds. |

## Native endpoint

Through the native Pushover API, this operation is `POST /groups/:group/add_user.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-user-to-group.md) for the provider-specific parameters and requirements.

