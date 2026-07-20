# Scrape do: List async jobs

Retrieves async jobs from Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/list-async-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/list-async-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/list-async-jobs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Jobs": [
        {}
      ],
      "PageNumber": 1,
      "PageSize": 1,
      "TotalCount": 1,
      "TotalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Jobs` | array<object> | Page of async jobs. |
| `PageNumber` | number | Current page number. |
| `PageSize` | number | Jobs per page. |
| `TotalCount` | number | Total number of jobs. |
| `TotalPages` | number | Total number of pages. |

## Native endpoint

Through the native Scrape do API, this operation is `GET https://q.scrape.do/api/v1/jobs` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-async-jobs.md) for the provider-specific parameters and requirements.

