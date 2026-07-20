# Dachser: List Transport Orders

Retrieves transport orders from Dachser within a date range.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/list-transport-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/list-transport-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/list-transport-orders?${params}`, {
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
| `dateFrom` | date | no | Filter transport orders from this date. |
| `dateTo` | date | no | Filter transport orders through this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "consignee": {},
      "consignor": {},
      "forwarder": {},
      "id": 1,
      "labelQuantity": 1,
      "links": [
        {}
      ],
      "references": [
        {}
      ],
      "state": "string",
      "transportDate": "2026-05-07T12:00:00.000Z",
      "weight": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `consignee` | object |  |
| `consignor` | object |  |
| `forwarder` | object |  |
| `id` | number |  |
| `labelQuantity` | number |  |
| `links` | array<object> |  |
| `references` | array<object> |  |
| `state` | string |  |
| `transportDate` | date |  |
| `weight` | object |  |

## Native endpoint

Through the native Dachser API, this operation is `GET /rest/v2/transportorders` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transport-orders.md) for the provider-specific parameters and requirements.

