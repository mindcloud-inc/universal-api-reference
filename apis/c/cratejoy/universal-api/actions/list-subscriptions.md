# Cratejoy: List Subscriptions

Retrieves subscriptions from Cratejoy.

```
GET https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-subscriptions?${params}`, {
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
      "autorenew": true,
      "credit": 1,
      "end_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "note": "string",
      "product_billing_id": 1,
      "skipped_date": "2026-05-07T12:00:00.000Z",
      "start_date": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autorenew` | boolean |  |
| `credit` | number |  |
| `end_date` | date |  |
| `id` | number |  |
| `note` | string |  |
| `product_billing_id` | number |  |
| `skipped_date` | date |  |
| `start_date` | date |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `GET /v1/subscriptions/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

