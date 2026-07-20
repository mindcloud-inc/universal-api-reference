# ConnectPay: Get BaaS Merchant Recurrence Details

Retrieves BaaS merchant recurrence details from ConnectPay.

```
GET https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-baas-merchant-recurrence-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConnectPay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-baas-merchant-recurrence-details?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-baas-merchant-recurrence-details?${params}`, {
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
| `recurrenceId` | string | no | Merchant recurrence ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ConnectPay API returns.

## Native endpoint

Through the native ConnectPay API, this operation is `GET /baas/merchant/recurrences/:recurrenceId` (base URL `https://api-stage.connectpay.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-baas-merchant-recurrence-details.md) for the provider-specific parameters and requirements.

