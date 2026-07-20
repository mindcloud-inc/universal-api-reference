# Sendloop: Subscribe Email Address



```
POST https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/subscribe-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/subscribe-email-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAddress": "ava@example.com",
  "listId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/subscribe-email-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAddress": "ava@example.com",
    "listId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | yes | The email address which is going to be subscribed |
| `listId` | number | yes | ID of the target subscriber list |
| `subscriptionIP` | string | no | IP address of the subscriber Default: `0.0.0.0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscriberID": "string",
      "subscriptionStatus": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscriberID` | string |  |
| `subscriptionStatus` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /subscriber.subscribe/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscribe-email-address.md) for the provider-specific parameters and requirements.

