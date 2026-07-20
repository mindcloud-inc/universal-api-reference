# Realcrux: Upsert Subscriber



```
POST https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/upsert-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Realcrux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/upsert-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "list_uid": "string",
  "EMAIL": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/realcrux/latest/actions/upsert-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "list_uid": "string",
    "EMAIL": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `list_uid` | string | yes | UID of the Sendcrux mail list that should receive or update the subscriber. |
| `EMAIL` | string | yes | Email address of the subscriber. The verified list contract marks EMAIL as required. |
| `FIRST_NAME` | string | no | First name field exposed by the verified Sendcrux list. |
| `LAST_NAME` | string | no | Last name field exposed by the verified Sendcrux list. |
| `COUNTRY` | string | no | Country field exposed by the verified Sendcrux list. |
| `PHONE_NUMBER` | string | no | Phone number field exposed by the verified Sendcrux list. |
| `COMPANY` | string | no | Company field exposed by the verified Sendcrux list. |

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
| `message` | string | Human-readable provider result message. |
| `status` | number | Provider success indicator. |
| `subscriber_uid` | string | UID of the created or updated subscriber record. |

## Native endpoint

Through the native Realcrux API, this operation is `POST subscribers` (base URL `https://sendcrux.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-subscriber.md) for the provider-specific parameters and requirements.

