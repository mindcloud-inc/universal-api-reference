# Bokun: Get Booking Payments

Retrieves customer payments for a booking from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-booking-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-booking-payments?connectionId=$CONNECTION_ID&bookingId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookingId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-booking-payments?${params}`, {
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
| `bookingId` | number | yes | The Bokun booking ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": "string",
      "comment": "string",
      "creationDate": 1,
      "currency": "string",
      "externalCardId": 1,
      "giftCardId": 1,
      "id": 1,
      "paymentProviderType": "string",
      "paymentReferenceId": "string",
      "paymentType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | string |  |
| `comment` | string |  |
| `creationDate` | number |  |
| `currency` | string |  |
| `externalCardId` | number |  |
| `giftCardId` | number |  |
| `id` | number |  |
| `paymentProviderType` | string |  |
| `paymentReferenceId` | string |  |
| `paymentType` | string |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/booking/:bookingId/payments` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-booking-payments.md) for the provider-specific parameters and requirements.

