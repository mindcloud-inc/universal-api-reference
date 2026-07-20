# ChargeOver: Record Usage

Creates a new metered usage record in ChargeOver.

```
POST https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/record-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeOver `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/record-usage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lineItemId": "string",
  "usageValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/record-usage', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lineItemId": "string",
    "usageValue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | no | Optional start date/time for the usage period. |
| `lineItemId` | string | yes | The subscription line item ID that the usage record belongs to. |
| `to` | string | no | Optional end date/time for the usage period. |
| `type` | string | no | Optional usage mode such as add, max, lat, pia, pas, or dlt. |
| `usageValue` | string | yes | The metered usage value to record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native ChargeOver API, this operation is `POST /usage` (base URL `https://{{credentials.siteName}}.chargeover.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-usage.md) for the provider-specific parameters and requirements.

