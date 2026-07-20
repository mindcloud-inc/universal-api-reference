# Doppler Marketing Automation: Unsubscribe Subscriber

Updates a subscriber to unsubscribed in Doppler Marketing Automation.

```
PUT https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/unsubscribe-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Marketing Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/unsubscribe-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "subscriber@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/unsubscribe-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "subscriber@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Subscriber email address to unsubscribe. Example: `subscriber@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": [
        {}
      ],
      "createdResourceId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | array<object> |  |
| `createdResourceId` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Doppler Marketing Automation API, this operation is `POST /accounts/:accountName/unsubscribed` (base URL `https://restapi.fromdoppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-subscriber.md) for the provider-specific parameters and requirements.

