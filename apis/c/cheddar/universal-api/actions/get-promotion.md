# Cheddar: Get Promotion

Retrieves promotion coupon details from Cheddar.

```
GET https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/get-promotion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cheddar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/get-promotion?connectionId=$CONNECTION_ID&promotionCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "promotionCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/get-promotion?${params}`, {
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
| `promotionCode` | string | yes | Promotion code from Cheddar. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "promotions": [
        {
          "code": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `promotions` | array<object> |  |
| `promotions[].code` | string |  |

## Native endpoint

Through the native Cheddar API, this operation is `GET /promotions/get/productCode/{{credentials.productCode}}/code/:promotionCode` (base URL `https://getcheddar.com/xml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-promotion.md) for the provider-specific parameters and requirements.

