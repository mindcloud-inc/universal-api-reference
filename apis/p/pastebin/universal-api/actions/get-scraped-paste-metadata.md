# Pastebin: Get Scraped Paste Metadata

Retrieves metadata for a scraped Pastebin paste.

```
GET https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/get-scraped-paste-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pastebin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/get-scraped-paste-metadata?connectionId=$CONNECTION_ID&pasteKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pasteKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pastebin/latest/actions/get-scraped-paste-metadata?${params}`, {
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
| `pasteKey` | string | yes | The public paste key to inspect through the scraping API metadata endpoint. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pastebin API returns.

## Native endpoint

Through the native Pastebin API, this operation is `GET https://scrape.pastebin.com/api_scrape_item_meta.php` (base URL `https://pastebin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scraped-paste-metadata.md) for the provider-specific parameters and requirements.

