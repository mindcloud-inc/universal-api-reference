# Scrape do: Get Amazon raw HTML

Retrieves Amazon raw HTML with Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-amazon-raw-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-amazon-raw-html?connectionId=$CONNECTION_ID&geocode=string&url=https%3A%2F%2Fexample.com&zipcode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "geocode": "string",
  "url": "https://example.com",
  "zipcode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/get-amazon-raw-html?${params}`, {
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
| `url` | string | yes | The full Amazon URL to fetch as raw HTML. |
| `zipcode` | string | yes | Postal code formatted for the selected marketplace. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scrape do API returns.

## Native endpoint

Through the native Scrape do API, this operation is `GET /plugin/amazon/` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-amazon-raw-html.md) for the provider-specific parameters and requirements.

