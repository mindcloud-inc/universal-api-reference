# CustomerX: Add Customer Journey

Creates a customer journey link in CustomerX.

```
POST https://connect.mindcloud.co/v1/universal/customerX/latest/actions/add-customer-journey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/add-customer-journey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/add-customer-journey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "default_journey_id": 1,
      "description": "string",
      "first_step_as_in_progress": true,
      "id": 1,
      "is_customized": true,
      "start_next_step_on_complete_step": true,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `default_journey_id` | number |  |
| `description` | string |  |
| `first_step_as_in_progress` | boolean |  |
| `id` | number |  |
| `is_customized` | boolean |  |
| `start_next_step_on_complete_step` | boolean |  |
| `updated_at` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `POST /api/v1/clients/journeys_clients` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-customer-journey.md) for the provider-specific parameters and requirements.

