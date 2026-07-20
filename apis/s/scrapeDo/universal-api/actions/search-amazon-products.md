# Scrape do: Search Amazon products

Finds Amazon products with Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/search-amazon-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/search-amazon-products?connectionId=$CONNECTION_ID&geocode=string&keyword=string&zipcode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "geocode": "string",
  "keyword": "string",
  "zipcode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/search-amazon-products?${params}`, {
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
| `geocode` | string | yes | Amazon marketplace country code such as us, gb, de, or jp. |
| `keyword` | string | yes | The Amazon search query. |
| `zipcode` | string | yes | Postal code formatted for the selected marketplace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorMessage": "string",
      "keyword": "string",
      "page": 1,
      "products": [
        {}
      ],
      "status": "string",
      "totalResults": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorMessage` | string | Error text when the request fails. |
| `keyword` | string | Amazon search keyword. |
| `page` | number | Current search results page. |
| `products` | array<object> | Search result products. |
| `status` | string | Request status. |
| `totalResults` | string | Human-readable result count. |

## Native endpoint

Through the native Scrape do API, this operation is `GET /plugin/amazon/search` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-amazon-products.md) for the provider-specific parameters and requirements.

