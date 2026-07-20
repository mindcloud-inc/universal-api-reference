# ScrapingDog: Get Google Scholar Author

Retrieves Google Scholar author details through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-scholar-author
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-scholar-author?connectionId=$CONNECTION_ID&authorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-scholar-author?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "articles": {
        "authors": "string",
        "citation_id": "string",
        "cited_by": {
          "citation_id": "string",
          "link": "https://example.com",
          "scrapingdog_link": "https://example.com",
          "value": "string"
        },
        "link": "https://example.com",
        "publication": "string",
        "title": "string",
        "year": "string"
      },
      "author": {
        "affiliations": "string",
        "email": "ava@example.com",
        "interests": {
          "link": "https://example.com",
          "title": "string"
        },
        "name": "Ava Chen",
        "thumbnail": "string"
      },
      "cited_by": {
        "graph": {
          "citations": "string",
          "year": "string"
        },
        "table": {
          "citations": {
            "all": 1,
            "since_2019": 1
          }
        }
      },
      "co_authors": {
        "affiliations": "string",
        "author_id": "string",
        "emails": "ava@example.com",
        "link": "https://example.com",
        "name": "Ava Chen",
        "scrapingdog_link": "https://example.com"
      },
      "pagination": {
        "next": "string"
      },
      "public_access": {
        "available": "string",
        "link": "https://example.com",
        "not_available": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articles` | array<object> |  |
| `articles.authors` | string |  |
| `articles.citation_id` | string |  |
| `articles.cited_by` | object |  |
| `articles.cited_by.citation_id` | string |  |
| `articles.cited_by.link` | string |  |
| `articles.cited_by.scrapingdog_link` | string |  |
| `articles.cited_by.value` | string |  |
| `articles.link` | string |  |
| `articles.publication` | string |  |
| `articles.title` | string |  |
| `articles.year` | string |  |
| `author` | object |  |
| `author.affiliations` | string |  |
| `author.email` | string |  |
| `author.interests` | array<object> |  |
| `author.interests.link` | string |  |
| `author.interests.title` | string |  |
| `author.name` | string |  |
| `author.thumbnail` | string |  |
| `cited_by` | object |  |
| `cited_by.graph` | array<object> |  |
| `cited_by.graph.citations` | string |  |
| `cited_by.graph.year` | string |  |
| `cited_by.table` | array<object> |  |
| `cited_by.table.citations` | object |  |
| `cited_by.table.citations.all` | number |  |
| `cited_by.table.citations.since_2019` | number |  |
| `co_authors` | array<object> |  |
| `co_authors.affiliations` | string |  |
| `co_authors.author_id` | string |  |
| `co_authors.emails` | string |  |
| `co_authors.link` | string |  |
| `co_authors.name` | string |  |
| `co_authors.scrapingdog_link` | string |  |
| `pagination` | object |  |
| `pagination.next` | string |  |
| `public_access` | object |  |
| `public_access.available` | string |  |
| `public_access.link` | string |  |
| `public_access.not_available` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_scholar/author` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-scholar-author.md) for the provider-specific parameters and requirements.

