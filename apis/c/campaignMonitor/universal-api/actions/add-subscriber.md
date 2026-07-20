# Campaign Monitor: Add Subscriber

Adds a subscriber to a Campaign Monitor list, or updates an existing one.

```
POST https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/add-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/add-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "string",
  "emailAddress": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/add-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "string",
    "emailAddress": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Campaign Monitor list identifier. |
| `emailAddress` | string | yes | Subscriber email address. |
| `name` | string | no | Subscriber name. |
| `resubscribe` | boolean | no | Whether to resubscribe the subscriber if previously unsubscribed. |
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
| `response` | string | Subscriber email address returned by Campaign Monitor when the subscriber is added. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `POST /subscribers/:listId.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subscriber.md) for the provider-specific parameters and requirements.

