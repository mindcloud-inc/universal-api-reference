# Olostep: List Crawl Pages

Retrieves pages from an Olostep crawl.

```
GET https://connect.mindcloud.co/v1/universal/olostep/latest/actions/list-crawl-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/list-crawl-pages?connectionId=$CONNECTION_ID&limit=25&offset=0&crawlId=crawl_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "crawlId": "crawl_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/list-crawl-pages?${params}`, {
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
| `crawlId` | string | yes | The ID of the crawl whose pages you want to list. Example: `crawl_123`. |
| `cursor` | number | no | Optional cursor index to continue listing crawl pages. Example: `0`. |
| `searchQuery` | string | no | Optional search query to sort crawl pages by relevance. Example: `documentation examples`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "pages": [
        {
          "id": "string",
          "isExternal": true,
          "retrieveId": "string",
          "url": "https://example.com"
        }
      ],
      "pagesCount": 1,
      "searchQuery": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `object` | string |  |
| `pages[].id` | string |  |
| `pages[].isExternal` | boolean |  |
| `pages[].retrieveId` | string |  |
| `pages[].url` | string |  |
| `pagesCount` | number |  |
| `searchQuery` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `GET /v1/crawls/[:crawl_id]/pages` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-crawl-pages.md) for the provider-specific parameters and requirements.

