# Sender: Remove Subscriber from Group



```
PUT https://connect.mindcloud.co/v1/universal/sender/latest/actions/remove-subscriber-from-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sender/latest/actions/remove-subscriber-from-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "grp_123",
  "subscribers[]": "user@example.com,another@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sender/latest/actions/remove-subscriber-from-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "grp_123",
    "subscribers[]": "user@example.com,another@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | Provide the group id. Example: `grp_123`. |
| `subscribers[]` | array<string> | yes | Array of email addresses that would be removed from this group. Example: `user@example.com,another@example.com`. |
| `conditions` | string | no | Select subscribers in bulk. Cannot be combined with subscribers. Example: `status=ACTIVE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Success message returned when subscribers are removed from a Sender group. |

## Native endpoint

Through the native Sender API, this operation is `DELETE /subscribers/groups/:groupId` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-subscriber-from-group.md) for the provider-specific parameters and requirements.

