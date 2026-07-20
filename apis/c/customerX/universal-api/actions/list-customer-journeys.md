# CustomerX: List Customer Journeys

Retrieves linked customer journeys from CustomerX.

```
GET https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-customer-journeys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-customer-journeys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-customer-journeys?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
      "customers_follow_ups_progress": [
        {}
      ],
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
| `customers_follow_ups_progress` | array<object> |  |
| `default_journey_id` | number |  |
| `description` | string |  |
| `first_step_as_in_progress` | boolean |  |
| `id` | number |  |
| `is_customized` | boolean |  |
| `start_next_step_on_complete_step` | boolean |  |
| `updated_at` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `GET /api/v1/clients/journeys_clients` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-journeys.md) for the provider-specific parameters and requirements.

