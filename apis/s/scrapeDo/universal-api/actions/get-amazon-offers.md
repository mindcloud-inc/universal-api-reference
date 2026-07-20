# Scrape do: Get Amazon offers

Retrieves Amazon offers with Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-amazon-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-amazon-offers?connectionId=$CONNECTION_ID&asin=string&geocode=string&zipcode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asin": "string",
  "geocode": "string",
  "zipcode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-amazon-offers?${params}`, {
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
| `asin` | string | yes | The 10-character Amazon product identifier. |
| `geocode` | string | yes | Amazon marketplace country code such as us, gb, de, or jp. |
| `zipcode` | string | yes | Postal code formatted for the selected marketplace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asin": "string",
      "errorMessage": "string",
      "offers": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asin` | string | Amazon product ASIN. |
| `errorMessage` | string | Error text when the request fails. |
| `offers` | array<object> | Seller offer entries. |
| `status` | string | Request status. |

## Native endpoint

Through the native Scrape do API, this operation is `GET /plugin/amazon/offer-listing` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-amazon-offers.md) for the provider-specific parameters and requirements.

