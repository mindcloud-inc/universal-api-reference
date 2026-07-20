# Customer.io: Get Segment Customer Count

Retrieves the customer count for a Customer.io segment.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-segment-customer-count
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-segment-customer-count?connectionId=$CONNECTION_ID&segmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "segmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-segment-customer-count?${params}`, {
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
| `segmentId` | list<number> | yes | The identifier for the segment to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "segmentId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | The total number of customers in the segment. |
| `segmentId` | number | The identifier for the segment. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/segments/:segment_id/customer_count` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-segment-customer-count.md) for the provider-specific parameters and requirements.

