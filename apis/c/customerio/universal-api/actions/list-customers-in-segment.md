# Customer.io: List Customers in a Segment

Retrieves customers in a segment from Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customers-in-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customers-in-segment?connectionId=$CONNECTION_ID&limit=25&offset=0&segmentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "segmentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customers-in-segment?${params}`, {
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
| `segmentId` | number | yes | The numeric ID of the segment whose members you want to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cioId": "string",
      "email": "ava@example.com",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cioId` | string | The Customer.io person identifier. |
| `email` | string | The customer email address. |
| `id` | string | The customer identifier. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/segments/:segment_id/membership` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers-in-segment.md) for the provider-specific parameters and requirements.

