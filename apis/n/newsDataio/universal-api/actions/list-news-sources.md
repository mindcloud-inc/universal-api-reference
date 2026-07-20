# NewsData.io: List News Sources



```
GET https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-news-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsData.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-news-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsDataio/latest/actions/list-news-sources?${params}`, {
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
| `category` | string | no | Category filter for source results. |
| `country` | string | no | Country code filter for source results. |
| `domainUrl` | string | no | Filter sources by one or more domain URLs. |
| `language` | string | no | Language code filter for source results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": "string",
      "results": [
        {}
      ],
      "status": "string",
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPage` | string | Pagination token for the next page when more results are available; may be empty or null on the last page. |
| `results` | array<object> | Returned source records. |
| `status` | string | Request status. |
| `totalResults` | number | Total number of returned source records in the current response. |

## Native endpoint

Through the native NewsData.io API, this operation is `GET /sources` (base URL `https://newsdata.io/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-news-sources.md) for the provider-specific parameters and requirements.

