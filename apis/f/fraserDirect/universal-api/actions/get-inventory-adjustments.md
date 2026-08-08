# Fraser Direct: Get inventory adjustments



```
GET https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-inventory-adjustments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fraser Direct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-inventory-adjustments?connectionId=$CONNECTION_ID&startDateTimeGmt=2025-01-01T03%3A47%3A22" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDateTimeGmt": "2025-01-01T03:47:22"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-inventory-adjustments?${params}`, {
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
| `startDateTimeGmt` | string | yes | Required UTC timestamp in yyyy-MM-ddTHH:mm:ss format. Example: `2025-01-01T03:47:22`. |
| `endDateTimeGmt` | string | no | Optional UTC timestamp in yyyy-MM-ddTHH:mm:ss format. When omitted, Fraser Direct returns all adjustments on or after StartDateTimeGMT. Example: `2025-02-25T23:59:59`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorList": [
        {}
      ],
      "inventoryAdjustmentList": [
        {}
      ],
      "success": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorList` | array<object> |  |
| `inventoryAdjustmentList` | array<object> |  |
| `success` | string |  |

## Native endpoint

Through the native Fraser Direct API, this operation is `GET /GetInventoryAdjustments` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-adjustments.md) for the provider-specific parameters and requirements.

