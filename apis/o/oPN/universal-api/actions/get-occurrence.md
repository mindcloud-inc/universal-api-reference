# OPN: Get Occurrence

Retrieves details for a schedule occurrence from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-occurrence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-occurrence?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-occurrence?${params}`, {
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
      "execute_time": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "message": "string",
      "object": "string",
      "processed_at": "string",
      "result": "string",
      "retry_on": "string",
      "scheduled_on": "string",
      "status": "string",
      "transfer_amount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `execute_time` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `message` | string |  |
| `object` | string |  |
| `processed_at` | string |  |
| `result` | string |  |
| `retry_on` | string |  |
| `scheduled_on` | string |  |
| `status` | string |  |
| `transfer_amount` | number |  |

## Native endpoint

Through the native OPN API, this operation is `GET /occurrences/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-occurrence.md) for the provider-specific parameters and requirements.

