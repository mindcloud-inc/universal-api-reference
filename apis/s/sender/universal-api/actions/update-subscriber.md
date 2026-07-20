# Sender: Update Subscriber



```
PUT https://connect.mindcloud.co/v1/universal/sender/latest/actions/update-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sender/latest/actions/update-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriberKey": "user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sender/latest/actions/update-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriberKey": "user@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriberKey` | string | yes | Subscriber email address, phone number, or ID. Example: `user@example.com`. |
| `firstName` | string | no | Updated first name. Example: `Jane`. |
| `lastName` | string | no | Updated last name. Example: `Doe`. |
| `groups[]` | array<string> | no | New groups assigned to the subscriber. Example: `grp_123,grp_456`. |
| `fields` | object | no | Provide field key-value pairs for the subscriber. Example: `[object Object]`. |
| `subscriberStatus` | string | no | One of ACTIVE, UNSUBSCRIBED, BOUNCED, or SPAM_REPORTED. Example: `ACTIVE`. |
| `phone` | string | no | Phone number must include the country code. Example: `+15551234567`. |
| `triggerAutomation` | boolean | no | Send false to avoid activating an automation. Example: `false`. |
| `smsStatus` | string | no | One of ACTIVE, UNSUBSCRIBED, BOUNCED, or SPAM_REPORTED. Example: `ACTIVE`. |
| `transactionalEmailStatus` | string | no | One of ACTIVE, UNSUBSCRIBED, BOUNCED, or SPAM_REPORTED. Example: `ACTIVE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array |  |
| `message` | string |  |

## Native endpoint

Through the native Sender API, this operation is `PATCH /subscribers/:subscriberKey` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscriber.md) for the provider-specific parameters and requirements.

