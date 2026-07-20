# ConnectPay: Get Card Authorisation Details

Retrieves card authorisation details from ConnectPay.

```
GET https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-card-authorisation-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConnectPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-card-authorisation-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-card-authorisation-details?${params}`, {
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
| `authorisationId` | string | no | Card authorisation ID. |
| `cardId` | string | no | Card ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ConnectPay API returns.

## Native endpoint

Through the native ConnectPay API, this operation is `GET /baas/ob/cards/:cardId/authorisation/:authorisationId` (base URL `https://api-stage.connectpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-card-authorisation-details.md) for the provider-specific parameters and requirements.

