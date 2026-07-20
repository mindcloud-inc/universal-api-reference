# Cartloom: Get Discount

Retrieves a discount record from Cartloom by ID.

```
GET https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/get-discount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cartloom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/get-discount?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cartloom/latest/actions/get-discount?${params}`, {
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
| `id` | string | yes | Internal discount ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowance": "string",
      "amount": "string",
      "auto": "string",
      "code": "string",
      "enabled": "string",
      "id": "string",
      "sid": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "stopDate": "2026-05-07T12:00:00.000Z",
      "target": "string",
      "type": "string",
      "used": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowance` | string | Maximum redemptions. |
| `amount` | string | Discount amount. |
| `auto` | string | Auto-apply flag. |
| `code` | string | Discount code. |
| `enabled` | string | Enabled flag. |
| `id` | string | Discount ID. |
| `sid` | string | Store-scoped ID. |
| `startDate` | date | Discount start date. |
| `stopDate` | date | Discount stop date. |
| `target` | string | Discount target. |
| `type` | string | Discount type. |
| `used` | string | Number of redemptions used. |

## Native endpoint

Through the native Cartloom API, this operation is `POST /discounts/get/format/json` (base URL `https://mindcloudstage0424.cartloom.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-discount.md) for the provider-specific parameters and requirements.

