# CallPage: Add Users To Widget

Adds users to an existing widget in CallPage.

```
PUT https://connect.mindcloud.co/v1/universal/callPage/latest/actions/add-users-to-widget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallPage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callPage/latest/actions/add-users-to-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "userIds": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callPage/latest/actions/add-users-to-widget', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "userIds": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `userIds` | list<number> | yes |  |
| `businessTimes` | list<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignment_id": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignment_id` | number |  |
| `user_id` | number |  |

## Native endpoint

Through the native CallPage API, this operation is `POST /widgets/add-users` (base URL `https://core.callpage.io/api/v1/external`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-users-to-widget.md) for the provider-specific parameters and requirements.

