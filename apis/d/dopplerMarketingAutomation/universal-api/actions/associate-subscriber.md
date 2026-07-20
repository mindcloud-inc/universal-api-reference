# Doppler Marketing Automation: Associate Subscriber

Creates a subscriber association in Doppler Marketing Automation.

```
POST https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/associate-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Doppler Marketing Automation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/associate-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "509702",
  "email": "subscriber@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/associate-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "509702",
    "email": "subscriber@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | Doppler list identifier. Example: `509702`. |
| `email` | string | yes | Subscriber email address. Example: `subscriber@example.com`. |
| `fields[]` | array<object> | no | Subscriber field values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": [
        {}
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
| `_links` | array<object> |  |
| `message` | string |  |

## Native endpoint

Through the native Doppler Marketing Automation API, this operation is `POST /accounts/:accountName/lists/:listId/subscribers` (base URL `https://restapi.fromdoppler.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/associate-subscriber.md) for the provider-specific parameters and requirements.

