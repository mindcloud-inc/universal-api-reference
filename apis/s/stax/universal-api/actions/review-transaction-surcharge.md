# Stax: Review Transaction Surcharge

Calculates surcharge details for a transaction in Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/review-transaction-surcharge
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/review-transaction-surcharge?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/review-transaction-surcharge?${params}`, {
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
| `paymentMethodId` | string | no | Payment method identifier |
| `total` | string | no | Transaction total for surcharge review |

## Response

```json
{
  "success": true,
  "data": [
    {
      "binType": "string",
      "surchargeAmount": 1,
      "surchargeRate": 1,
      "totalWithSurchargeAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `binType` | string | Detected card BIN type. |
| `surchargeAmount` | number | Calculated surcharge amount. |
| `surchargeRate` | number | Applicable surcharge rate. |
| `totalWithSurchargeAmount` | number | Total amount including surcharge. |

## Native endpoint

Through the native Stax API, this operation is `GET /surcharge/review` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/review-transaction-surcharge.md) for the provider-specific parameters and requirements.

