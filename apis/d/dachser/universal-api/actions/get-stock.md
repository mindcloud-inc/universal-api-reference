# Dachser: Get Stock

Retrieves stock records from Dachser by article or warehouse.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-stock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-stock?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-stock?${params}`, {
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
| `articleNumber` | string | no | Filter on article number. |
| `lot` | string | no | Filter on lot number. |
| `bestBeforeDate` | date | no | Filter on best-before date. |
| `customerId` | string | no | Customer number. |
| `branchId` | string | no | Warehouse or branch number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productVariant` | number | no | Filter on product variant. |
| `variableClassification` | number | no | Filter on variable classification. |
| `blockingReason` | number | no | Filter on blocking reason. |
| `acceptLanguage` | string | no | Optional language sent as the Accept-Language header. |
| `accept` | string | no | Optional Accept header value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articles": [
        {}
      ],
      "responseItems": [
        {}
      ],
      "storageCustomer": {},
      "warehouse": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articles` | array<object> |  |
| `responseItems` | array<object> |  |
| `storageCustomer` | object |  |
| `warehouse` | object |  |

## Native endpoint

Through the native Dachser API, this operation is `GET /rest/v2/stocks` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stock.md) for the provider-specific parameters and requirements.

