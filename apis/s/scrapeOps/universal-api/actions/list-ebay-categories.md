# ScrapeOps: List Ebay Categories

Retrieves eBay category data from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-ebay-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-ebay-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-ebay-categories?${params}`, {
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
| `url` | string | no | Full eBay category URL to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Category name. |
| `url` | string | Category URL. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/ebay/category` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ebay-categories.md) for the provider-specific parameters and requirements.

