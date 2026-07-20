# Pilvio: Get Billing Account Details



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-billing-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-billing-account-details?connectionId=$CONNECTION_ID&billingAccountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "billingAccountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/get-billing-account-details?${params}`, {
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
| `billingAccountId` | string | yes | Billing account ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalData": "string",
      "addressLine1": "string",
      "allowDebt": true,
      "canPay": true,
      "city": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalData` | string |  |
| `addressLine1` | string |  |
| `allowDebt` | boolean |  |
| `canPay` | boolean |  |
| `city` | string |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /payment/billing_account` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing-account-details.md) for the provider-specific parameters and requirements.

