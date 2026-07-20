# Ship24: Resend Tracker Webhook Events

Resends webhook events for an existing Ship24 tracker.

```
POST https://connect.mindcloud.co/v1/universal/ship24/latest/actions/resend-tracker-webhook-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/resend-tracker-webhook-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackerId": "26148317-7502-d3ac-44a9-546d240ac0dd"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ship24/latest/actions/resend-tracker-webhook-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trackerId": "26148317-7502-d3ac-44a9-546d240ac0dd"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trackerId` | string | yes | Ship24 tracker ID returned when the tracker was created. Example: `26148317-7502-d3ac-44a9-546d240ac0dd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "summary": {
        "totalResent": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `summary.totalResent` | number | Total number of webhook events resent. |

## Native endpoint

Through the native Ship24 API, this operation is `POST /public/v1/trackers/:trackerId/webhook-events/resend` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resend-tracker-webhook-events.md) for the provider-specific parameters and requirements.

