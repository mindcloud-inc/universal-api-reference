# ScrapeOps: List Ebay Feedback

Retrieves eBay feedback from ScrapeOps.

```
GET https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-ebay-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-ebay-feedback?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOps/latest/actions/list-ebay-feedback?${params}`, {
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
| `url` | string | no | Full eBay seller profile URL whose feedback to list. |
| `username` | string | no | eBay seller username whose feedback to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "item_id": "string",
      "item_link": "https://example.com",
      "item_name": "Ava Chen",
      "price": "string",
      "rating": "string",
      "user": "string",
      "user_score": 1,
      "when": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | Feedback comment. |
| `item_id` | string | Item ID. |
| `item_link` | string | Item link. |
| `item_name` | string | Item name. |
| `price` | string | Item price text. |
| `rating` | string | Feedback rating. |
| `user` | string | Feedback user. |
| `user_score` | number | Feedback user score. |
| `when` | string | Relative feedback time. |

## Native endpoint

Through the native ScrapeOps API, this operation is `GET https://proxy.scrapeops.io/v1/structured-data/ebay/feedback` (base URL `http://headers.scrapeops.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ebay-feedback.md) for the provider-specific parameters and requirements.

