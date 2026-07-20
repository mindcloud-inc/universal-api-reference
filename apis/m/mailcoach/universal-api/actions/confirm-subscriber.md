# Mailcoach: Confirm Subscriber

Confirms an existing subscriber in Mailcoach.

```
PUT https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/confirm-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcoach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/confirm-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/confirm-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | The UUID of the subscriber to confirm. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `uuid` | string |  |

## Native endpoint

Through the native Mailcoach API, this operation is `POST /subscribers/:uuid/confirm` (base URL `https://mindcloud.mailcoach.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/confirm-subscriber.md) for the provider-specific parameters and requirements.

