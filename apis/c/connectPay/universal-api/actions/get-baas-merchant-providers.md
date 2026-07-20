# ConnectPay: Get BaaS Merchant Providers

Retrieves BaaS merchant providers from ConnectPay.

```
GET https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-baas-merchant-providers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConnectPay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-baas-merchant-providers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-baas-merchant-providers?${params}`, {
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
| `BaaSClientBrandId` | string | no | Merchant brand identifier provided by ConnectPay. |
| `countryCode` | string | no | Provider country code, for example DE, NL, or LT. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ConnectPay API returns.

## Native endpoint

Through the native ConnectPay API, this operation is `GET /baas/merchant/brands/:BaaSClientBrandId/providers` (base URL `https://api-stage.connectpay.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-baas-merchant-providers.md) for the provider-specific parameters and requirements.

