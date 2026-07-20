# Edoobox: Get Offer

Retrieves details for an offer from Edoobox.

```
GET https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-offer?connectionId=$CONNECTION_ID&offerId=offer_3faa29c0777e_7511450890" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "offerId": "offer_3faa29c0777e_7511450890"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/get-offer?${params}`, {
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
| `offerId` | string | yes | The edoobox offer ID to retrieve. Default: `offer_3faa29c0777e_7511450890`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archive": true,
      "barcodeTicket": true,
      "category": "string",
      "countdown": true,
      "country": "string",
      "dateClose": true,
      "dateDisplayend": 1,
      "dateDisplayendReference": "string",
      "dateDisplaystart": true,
      "dateEnd": true,
      "dateSignupstart": true,
      "dateStart": true,
      "design": true,
      "id": "string",
      "image": true,
      "internalCode": "string",
      "lessonBooking": true,
      "mode": "string",
      "multiOffer": true,
      "multiOfferChild": true,
      "multipleRegistration": true,
      "multipleRegistrationType": "string",
      "mustpay": true,
      "name": "Ava Chen",
      "number": "string",
      "offerdef": "string",
      "order": 1,
      "place": true,
      "rowLft": 1,
      "rowRgt": 1,
      "shortdescription": "string",
      "status": 1,
      "trash": true,
      "type": "string",
      "userMaximum": 1,
      "userMinimal": 1,
      "vat": true,
      "waitingList": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archive` | boolean |  |
| `barcodeTicket` | boolean |  |
| `category` | string |  |
| `countdown` | boolean |  |
| `country` | string |  |
| `dateClose` | boolean |  |
| `dateDisplayend` | number |  |
| `dateDisplayendReference` | string |  |
| `dateDisplaystart` | boolean |  |
| `dateEnd` | boolean |  |
| `dateSignupstart` | boolean |  |
| `dateStart` | boolean |  |
| `design` | boolean |  |
| `id` | string |  |
| `image` | boolean |  |
| `internalCode` | string |  |
| `lessonBooking` | boolean |  |
| `mode` | string |  |
| `multiOffer` | boolean |  |
| `multiOfferChild` | boolean |  |
| `multipleRegistration` | boolean |  |
| `multipleRegistrationType` | string |  |
| `mustpay` | boolean |  |
| `name` | string |  |
| `number` | string |  |
| `offerdef` | string |  |
| `order` | number |  |
| `place` | boolean |  |
| `rowLft` | number |  |
| `rowRgt` | number |  |
| `shortdescription` | string |  |
| `status` | number |  |
| `trash` | boolean |  |
| `type` | string |  |
| `userMaximum` | number |  |
| `userMinimal` | number |  |
| `vat` | boolean |  |
| `waitingList` | boolean |  |

## Native endpoint

Through the native Edoobox API, this operation is `GET /offer/:offer_id` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-offer.md) for the provider-specific parameters and requirements.

