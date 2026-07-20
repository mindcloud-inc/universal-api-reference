# Sendcrux: Update Subscriber

Updates an existing subscriber in Sendcrux.

```
PUT https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/update-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/update-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "EMAIL": "ava@example.com",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendcrux/latest/actions/update-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "EMAIL": "ava@example.com",
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `EMAIL` | string | yes | The subscriber email address that Sendcrux requires on update. |
| `FIRST_NAME` | string | no | The subscriber first name. |
| `LAST_NAME` | string | no | The subscriber last name. |
| `tag` | string | no | A comma-separated list of tags to persist on the subscriber. |
| `uid` | string | yes | The unique identifier of the subscriber to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1,
      "subscriber_uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | number |  |
| `subscriber_uid` | string |  |

## Native endpoint

Through the native Sendcrux API, this operation is `PATCH /api/v1/subscribers/:uid` (base URL `https://sendcrux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber.md) for the provider-specific parameters and requirements.

