# PostcardMania: List Batch Orders

Retrieves orders from a PostcardMania batch.

```
GET https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-batch-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PostcardMania `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-batch-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postcardMania/latest/actions/list-batch-orders?${params}`, {
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
| `batchID` | string | no | Internal batch identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Pagination metadata. |
| `results` | array<object> | Orders in the requested batch. |

## Native endpoint

Through the native PostcardMania API, this operation is `GET /batch/{{batchID}}/orders` (base URL `https://v3.pcmintegrations.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-batch-orders.md) for the provider-specific parameters and requirements.

