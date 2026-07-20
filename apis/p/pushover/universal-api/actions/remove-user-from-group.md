# Pushover: Remove User from Group



```
DELETE https://connect.mindcloud.co/v1/universal/pushover/latest/actions/remove-user-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushover `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pushover/latest/actions/remove-user-from-group?connectionId=$CONNECTION_ID&group=string&user=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "string",
  "user": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushover/latest/actions/remove-user-from-group?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group` | string | yes | Delivery group key identifying which group to modify. |
| `user` | string | yes | Pushover user key to remove from the group. |
| `device` | string | no | Optional device name to match when removing the user from the group. |

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
| `status` | number | API status. Returns 1 when the remove-user request succeeds. |

## Native endpoint

Through the native Pushover API, this operation is `POST /groups/:group/remove_user.json` (base URL `https://api.pushover.net/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-user-from-group.md) for the provider-specific parameters and requirements.

