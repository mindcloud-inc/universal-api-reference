# Campaign Monitor: Update Subscriber

Updates an existing subscriber in a Campaign Monitor list.

```
PUT https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/update-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/update-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/update-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Campaign Monitor list identifier. |
| `email` | string | yes | Subscriber email address to update. |
| `emailAddress` | string | no | New subscriber email address. |
| `name` | string | no | Subscriber name. |
| `resubscribe` | boolean | no | Whether to resubscribe the subscriber if previously unsubscribed. |
| `restartSubscriptionBasedAutoresponders` | boolean | no | Whether to restart subscription-based autoresponders. |
| `consentToTrack` | string | no | Consent-to-track value for the subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Empty string on success because Campaign Monitor returns HTTP 200 OK with no response body for subscriber updates. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `PUT /subscribers/:listId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber.md) for the provider-specific parameters and requirements.

