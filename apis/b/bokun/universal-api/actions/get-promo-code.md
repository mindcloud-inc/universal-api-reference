# Bokun: Get Promo Code

Retrieves a promo code by ID from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-promo-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-promo-code?connectionId=$CONNECTION_ID&promoCodeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "promoCodeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/get-promo-code?${params}`, {
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
| `promoCodeId` | number | yes | The Bokun promo code ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookingValidFrom": "2026-05-07T12:00:00.000Z",
      "bookingValidTo": "2026-05-07T12:00:00.000Z",
      "code": "string",
      "description": "string",
      "discountAmount": 1,
      "discountAmountCurrency": "string",
      "discountAmountPerPerson": true,
      "discountPercentage": 1,
      "discountPercentageAppliesToExtras": true,
      "discountPercentageAppliesToPickupAndDropoff": true,
      "id": 1,
      "maxUsages": 1,
      "travelValidDaysOfWeek": [
        "string"
      ],
      "travelValidFrom": "2026-05-07T12:00:00.000Z",
      "travelValidMonths": [
        "string"
      ],
      "travelValidTo": "2026-05-07T12:00:00.000Z",
      "validForAllProducts": true,
      "validForProducts": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookingValidFrom` | date |  |
| `bookingValidTo` | date |  |
| `code` | string |  |
| `description` | string |  |
| `discountAmount` | number |  |
| `discountAmountCurrency` | string |  |
| `discountAmountPerPerson` | boolean |  |
| `discountPercentage` | number |  |
| `discountPercentageAppliesToExtras` | boolean |  |
| `discountPercentageAppliesToPickupAndDropoff` | boolean |  |
| `id` | number |  |
| `maxUsages` | number |  |
| `travelValidDaysOfWeek` | array<string> |  |
| `travelValidFrom` | date |  |
| `travelValidMonths` | array<string> |  |
| `travelValidTo` | date |  |
| `validForAllProducts` | boolean |  |
| `validForProducts` | array<number> |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/promo/code/:promoCodeId` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-promo-code.md) for the provider-specific parameters and requirements.

