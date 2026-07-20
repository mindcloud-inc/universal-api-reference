# WebinarGeek: Retrieve Subscription



```
GET https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/retrieve-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebinarGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/retrieve-subscription?connectionId=$CONNECTION_ID&subscriptionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/retrieve-subscription?${params}`, {
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
| `subscriptionId` | number | yes | ID of the subscription to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confirmationLink": "https://example.com",
      "createdAt": 1,
      "eligibleToWatch": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "firstname": "Ava",
      "id": 1,
      "unsubscribed": true,
      "watchLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmationLink` | string |  |
| `createdAt` | number |  |
| `eligibleToWatch` | boolean |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `firstname` | string |  |
| `id` | number |  |
| `unsubscribed` | boolean |  |
| `watchLink` | string |  |

## Native endpoint

Through the native WebinarGeek API, this operation is `GET /subscriptions/:subscriptionId` (base URL `https://app.webinargeek.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-subscription.md) for the provider-specific parameters and requirements.

