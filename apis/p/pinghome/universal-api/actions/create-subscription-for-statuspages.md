# Pinghome: Create Subscription For Statuspages

Creates a new statuspage subscription in Pinghome.

```
POST https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-subscription-for-statuspages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-subscription-for-statuspages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelType": "email",
  "channelValue": "apps@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/create-subscription-for-statuspages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelType": "email",
    "channelValue": "apps@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelType` | string | yes | Notification channel type. Example: `email`. |
| `domain` | string | no | Statuspage domain or subdomain used to locate the statuspage for the subscription. |
| `channelValue` | string | yes | Notification channel value. Example: `apps@mindcloud.co`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `POST /statuspage-cmd/v1/subscriptions` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription-for-statuspages.md) for the provider-specific parameters and requirements.

