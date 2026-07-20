# InflatableOffice: Create Payment

Creates a payment in InflatableOffice.

```
POST https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/create-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leadid` | string | no |  |
| `manual` | string | no |  |
| `orderid` | string | no |  |
| `payamt` | string | no |  |
| `paystat` | string | no |  |
| `processor` | string | no |  |
| `reasoncode` | string | no |  |
| `surcharge` | string | no |  |
| `time` | string | no |  |
| `tip` | string | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "id": "string",
      "itemnum": "string",
      "payamt": "string",
      "paystat": "string",
      "processor": "string",
      "reasoncode": "string",
      "requestTime": 1,
      "source": "string",
      "time": "string",
      "txnid": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Currency code. |
| `id` | string | Created payment ID. |
| `itemnum` | string | Lead ID associated with the payment. |
| `payamt` | string | Payment amount. |
| `paystat` | string | Payment status. |
| `processor` | string | Payment processor label. |
| `reasoncode` | string | Provider reason code or note. |
| `requestTime` | number | Provider request timestamp. |
| `source` | string | Payment source label. |
| `time` | string | Payment timestamp supplied to the provider. |
| `txnid` | string | Transaction reference number. |
| `type` | string | Payment type. |

## Native endpoint

Through the native InflatableOffice API, this operation is `POST /handle_payment` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment.md) for the provider-specific parameters and requirements.

