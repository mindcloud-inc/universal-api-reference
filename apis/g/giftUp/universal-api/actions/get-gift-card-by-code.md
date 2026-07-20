# Gift Up: Get Gift Card by Code



```
GET https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-gift-card-by-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-gift-card-by-code?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/get-gift-card-by-code?${params}`, {
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
| `code` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backingType": "string",
      "canBeRedeemed": true,
      "cancelledOn": true,
      "code": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "downloadLinks": {},
      "emailFulfilment": {},
      "equivalentValuePerUnit": 1,
      "expiresOn": "2026-05-07T12:00:00.000Z",
      "fulfilledBy": "string",
      "fulfilledOn": "2026-05-07T12:00:00.000Z",
      "hasExpired": true,
      "imageUrl": "https://example.com",
      "initialUnits": 1,
      "initialValue": 1,
      "isProvisional": true,
      "isVoided": true,
      "ledger": [
        "string"
      ],
      "message": "string",
      "notYetValid": true,
      "order": {},
      "orderId": "string",
      "postalFulfilment": {},
      "purchaserName": "Ava Chen",
      "recipientEmail": "ava@example.com",
      "recipientName": "Ava Chen",
      "remainingUnits": 1,
      "remainingValue": 1,
      "sku": "string",
      "subTitle": "string",
      "terms": "string",
      "title": "string",
      "validFrom": "2026-05-07T12:00:00.000Z",
      "validOnDays": [
        "string"
      ],
      "voidedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backingType` | string |  |
| `canBeRedeemed` | boolean |  |
| `cancelledOn` | boolean |  |
| `code` | string |  |
| `createdOn` | date |  |
| `description` | string |  |
| `downloadLinks` | object |  |
| `emailFulfilment` | object |  |
| `equivalentValuePerUnit` | number |  |
| `expiresOn` | date |  |
| `fulfilledBy` | string |  |
| `fulfilledOn` | date |  |
| `hasExpired` | boolean |  |
| `imageUrl` | string |  |
| `initialUnits` | number |  |
| `initialValue` | number |  |
| `isProvisional` | boolean |  |
| `isVoided` | boolean |  |
| `ledger` | array<string> |  |
| `message` | string |  |
| `notYetValid` | boolean |  |
| `order` | object |  |
| `orderId` | string |  |
| `postalFulfilment` | object |  |
| `purchaserName` | string |  |
| `recipientEmail` | string |  |
| `recipientName` | string |  |
| `remainingUnits` | number |  |
| `remainingValue` | number |  |
| `sku` | string |  |
| `subTitle` | string |  |
| `terms` | string |  |
| `title` | string |  |
| `validFrom` | date |  |
| `validOnDays` | array<string> |  |
| `voidedOn` | date |  |

## Native endpoint

Through the native Gift Up API, this operation is `GET /gift-cards/:code` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gift-card-by-code.md) for the provider-specific parameters and requirements.

