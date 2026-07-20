# Eventix: Get attached PaymentMethods of Shop

Retrieves payment methods for an Eventix shop.

```
GET https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shop-specific-payment-methods
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shop-specific-payment-methods?connectionId=$CONNECTION_ID&guid=shop-guid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "shop-guid"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventix/latest/actions/get-shop-specific-payment-methods?${params}`, {
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
| `guid` | string | yes | The guid of the Shop. Example: `shop-guid`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "guid": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guid` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Eventix API, this operation is `GET /3.0.0/shop/:guid/payment_methods` (base URL `https://api.weeztix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shop-specific-payment-methods.md) for the provider-specific parameters and requirements.

