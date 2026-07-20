# Cituro: Get Discount

Retrieves a discount record from Cituro.

```
GET https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-discount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cituro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-discount?connectionId=$CONNECTION_ID&discountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "discountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cituro/latest/actions/get-discount?${params}`, {
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
| `discountId` | string | yes | Cituro discount identifier from the discount resource path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Unique Cituro discount identifier. |

## Native endpoint

Through the native Cituro API, this operation is `GET /discounts/:discountId` (base URL `https://app.cituro.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-discount.md) for the provider-specific parameters and requirements.

