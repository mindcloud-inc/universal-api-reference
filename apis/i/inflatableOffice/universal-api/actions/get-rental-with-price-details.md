# InflatableOffice: Get Rental With Price Details

Retrieves a rental with price details from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-rental-with-price-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-rental-with-price-details?connectionId=$CONNECTION_ID&rentalId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "rentalId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/get-rental-with-price-details?${params}`, {
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
| `rentalId` | string | yes | ID of the rental to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allcats": {},
      "description": "string",
      "href": "string",
      "id": "string",
      "imageloc": "string",
      "imagelocbig": "string",
      "images": {},
      "options": [
        "string"
      ],
      "prices": {},
      "requestTime": 1,
      "ridename": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allcats` | object |  |
| `description` | string |  |
| `href` | string |  |
| `id` | string |  |
| `imageloc` | string |  |
| `imagelocbig` | string |  |
| `images` | object |  |
| `options` | array<string> |  |
| `prices` | object |  |
| `requestTime` | number |  |
| `ridename` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /rentals/:rentalId` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rental-with-price-details.md) for the provider-specific parameters and requirements.

