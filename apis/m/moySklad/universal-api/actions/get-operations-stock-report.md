# MoySklad: Get operations stock report

Retrieves the operations stock report from MoySklad.

```
GET https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-operations-stock-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoySklad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-operations-stock-report?connectionId=$CONNECTION_ID&filter=assortment%3Dhttps%3A%2F%2Fapi.moysklad.ru%2Fapi%2Fremap%2F1.2%2Fentity%2Fproduct%2F89e05606-3ce8-11f1-0a80-161100021282" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filter": "assortment=https://api.moysklad.ru/api/remap/1.2/entity/product/89e05606-3ce8-11f1-0a80-161100021282"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moySklad/latest/actions/get-operations-stock-report?${params}`, {
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
| `filter` | string | yes | MoySklad filter argument. Default: `assortment=https://api.moysklad.ru/api/remap/1.2/entity/product/89e05606-3ce8-11f1-0a80-161100021282`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": {},
      "meta": {},
      "rows": [
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
| `context` | object |  |
| `meta` | object |  |
| `rows` | array<object> |  |

## Native endpoint

Through the native MoySklad API, this operation is `GET report/byoperations/stock` (base URL `https://api.moysklad.ru/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-operations-stock-report.md) for the provider-specific parameters and requirements.

