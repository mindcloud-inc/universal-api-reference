# Voucherify: Get Redemption

Retrieves a redemption from Voucherify.

```
GET https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-redemption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voucherify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-redemption?connectionId=$CONNECTION_ID&redemptionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "redemptionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucherify/latest/actions/get-redemption?${params}`, {
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
| `redemptionId` | string | yes | Voucherify redemption identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "order": {},
      "redeemables": [
        {}
      ],
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `object` | string |  |
| `order` | object |  |
| `redeemables` | array<object> |  |
| `result` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Voucherify API, this operation is `GET /redemptions/:redemptionId` (base URL `https://us1.api.voucherify.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-redemption.md) for the provider-specific parameters and requirements.

