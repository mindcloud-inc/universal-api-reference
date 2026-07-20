# Simpro: List Catalogs



```
GET https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-catalogs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-catalogs?connectionId=$CONNECTION_ID&companyId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpro/latest/actions/list-catalogs?${params}`, {
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
| `companyId` | string | yes | The Simpro company ID. Example: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "partNo": "string",
      "splitPrice": 1,
      "splitPriceEx": 1,
      "splitPriceInc": 1,
      "tradePrice": 1,
      "tradePriceEx": 1,
      "tradePriceInc": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `partNo` | string |  |
| `splitPrice` | number |  |
| `splitPriceEx` | number |  |
| `splitPriceInc` | number |  |
| `tradePrice` | number |  |
| `tradePriceEx` | number |  |
| `tradePriceInc` | number |  |

## Native endpoint

Through the native Simpro API, this operation is `GET /companies/:companyId/catalogs/` (base URL `https://mindcloud.simprosuite.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-catalogs.md) for the provider-specific parameters and requirements.

