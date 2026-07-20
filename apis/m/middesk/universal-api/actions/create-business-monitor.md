# Middesk: Create a monitor for a business

Creates a business monitor in Middesk.

```
POST https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-business-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-business-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": "string",
  "eventTypes[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/middesk/latest/actions/create-business-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": "string",
    "eventTypes[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessId` | string | yes | ID of the business to create a monitor for. |
| `eventTypes[]` | array | yes | Event types to monitor for the business. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native Middesk API, this operation is `POST /businesses/:business_id/monitor` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-business-monitor.md) for the provider-specific parameters and requirements.

