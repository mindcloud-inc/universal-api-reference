# CrowdPower: Get Customer Events

Retrieves events for a customer in CrowdPower.

```
GET https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customer-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrowdPower `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customer-events?connectionId=$CONNECTION_ID&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crowdPower/latest/actions/get-customer-events?${params}`, {
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
| `customerId` | string | yes | Customer identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "customer_id": "string",
      "event": {},
      "id": "string",
      "properties": {},
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number |  |
| `customer_id` | string |  |
| `event` | object |  |
| `id` | string |  |
| `properties` | object |  |
| `updated_at` | number |  |

## Native endpoint

Through the native CrowdPower API, this operation is `GET customers/:customer_id/events` (base URL `https://api.crowdpower.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-events.md) for the provider-specific parameters and requirements.

