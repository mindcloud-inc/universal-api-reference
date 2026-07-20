# Hiboutik: List Open Sales

Retrieves open sales for a store in Hiboutik.

```
GET https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-open-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hiboutik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-open-sales?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hiboutik/latest/actions/list-open-sales?${params}`, {
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
| `storeId` | string | no | The Hiboutik store id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customersId": 1,
      "saleId": 1,
      "total": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customersId` | number |  |
| `saleId` | number |  |
| `total` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Hiboutik API, this operation is `GET /open_sales/:store_id` (base URL `https://mindcloudhiboutik20260402.hiboutik.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-open-sales.md) for the provider-specific parameters and requirements.

