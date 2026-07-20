# ScrapingDog: Get Google Scholar Author Citation

Retrieves Google Scholar author citations through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-scholar-author-citation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-scholar-author-citation?connectionId=$CONNECTION_ID&authorId=string&citationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authorId": "string",
  "citationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-scholar-author-citation?${params}`, {
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
| `authorId` | string | yes | Google Scholar author identifier. |
| `citationId` | string | yes | Citation identifier returned by the Google Scholar author response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "citations": {
        "authors": "string",
        "description": "string",
        "journal": "string",
        "link": "https://example.com",
        "pages": "string",
        "publication_date": "string",
        "publisher": "string",
        "resources": {
          "file_format": "string",
          "link": "https://example.com",
          "title": "string"
        },
        "scholar_articles": {
          "authors": "string",
          "cited_by": {
            "cites_id": "string",
            "link": "https://example.com",
            "scrapingdog_link": "https://example.com",
            "total": "string"
          },
          "link": "https://example.com",
          "title": "string",
          "versions": {
            "cluster_id": "string",
            "link": "https://example.com",
            "scrapingdog_link": "https://example.com",
            "total": "string"
          }
        },
        "title": "string",
        "total_citations": {
          "cited_by": {
            "cites_id": "string",
            "link": "https://example.com",
            "scrapingdog_link": "https://example.com",
            "total": "string"
          },
          "table": {
            "citations": "string",
            "year": "string"
          }
        },
        "volume": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `citations` | object |  |
| `citations.authors` | string |  |
| `citations.description` | string |  |
| `citations.journal` | string |  |
| `citations.link` | string |  |
| `citations.pages` | string |  |
| `citations.publication_date` | string |  |
| `citations.publisher` | string |  |
| `citations.resources` | array<object> |  |
| `citations.resources.file_format` | string |  |
| `citations.resources.link` | string |  |
| `citations.resources.title` | string |  |
| `citations.scholar_articles` | array<object> |  |
| `citations.scholar_articles.authors` | string |  |
| `citations.scholar_articles.cited_by` | object |  |
| `citations.scholar_articles.cited_by.cites_id` | string |  |
| `citations.scholar_articles.cited_by.link` | string |  |
| `citations.scholar_articles.cited_by.scrapingdog_link` | string |  |
| `citations.scholar_articles.cited_by.total` | string |  |
| `citations.scholar_articles.link` | string |  |
| `citations.scholar_articles.title` | string |  |
| `citations.scholar_articles.versions` | object |  |
| `citations.scholar_articles.versions.cluster_id` | string |  |
| `citations.scholar_articles.versions.link` | string |  |
| `citations.scholar_articles.versions.scrapingdog_link` | string |  |
| `citations.scholar_articles.versions.total` | string |  |
| `citations.title` | string |  |
| `citations.total_citations` | object |  |
| `citations.total_citations.cited_by` | object |  |
| `citations.total_citations.cited_by.cites_id` | string |  |
| `citations.total_citations.cited_by.link` | string |  |
| `citations.total_citations.cited_by.scrapingdog_link` | string |  |
| `citations.total_citations.cited_by.total` | string |  |
| `citations.total_citations.table` | array<object> |  |
| `citations.total_citations.table.citations` | string |  |
| `citations.total_citations.table.year` | string |  |
| `citations.volume` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_scholar/author` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-scholar-author-citation.md) for the provider-specific parameters and requirements.

