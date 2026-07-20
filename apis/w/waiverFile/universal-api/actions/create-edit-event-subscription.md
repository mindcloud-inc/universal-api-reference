# WaiverFile: Create Edit Event Subscription

Creates an edit event subscription in WaiverFile.

```
POST https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/create-edit-event-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/create-edit-event-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/create-edit-event-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WaiverFile API returns.

## Native endpoint

Through the native WaiverFile API, this operation is `POST /subscribe/editevent` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-edit-event-subscription.md) for the provider-specific parameters and requirements.

