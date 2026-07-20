# Prodigi: Get Photobook Spine Details

Retrieves the required spine width for a Prodigi photobook.

```
GET https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-photobook-spine-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prodigi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-photobook-spine-details?connectionId=$CONNECTION_ID&sku=BOOK-A4-L-HARD-M&destinationCountryCode=US&numberOfPages=50" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sku": "BOOK-A4-L-HARD-M",
  "destinationCountryCode": "US",
  "numberOfPages": "50"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/get-photobook-spine-details?${params}`, {
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
| `sku` | string | yes | Photobook product SKU. Example: `BOOK-A4-L-HARD-M`. |
| `destinationCountryCode` | string | yes | Two-letter ISO country code for the destination country. Example: `US`. |
| `numberOfPages` | number | yes | Number of pages in the photobook. Example: `50`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `state` | string | no | Destination state, used when needed for the destination country. Example: `CA`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "widthMm": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `widthMm` | number | Required book spine width in millimeters. |

## Native endpoint

Through the native Prodigi API, this operation is `POST /products/spine` (base URL `https://api.prodigi.com/v4.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-photobook-spine-details.md) for the provider-specific parameters and requirements.

