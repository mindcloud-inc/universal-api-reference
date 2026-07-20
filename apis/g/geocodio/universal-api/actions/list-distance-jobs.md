# Geocodio: List Distance Jobs

Retrieves asynchronous distance jobs from Geocodio.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/list-distance-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/list-distance-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/list-distance-jobs?${params}`, {
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
      "data": [
        {
          "calculationsCompleted": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "destinationsCount": 1,
          "distanceMode": "string",
          "downloadUrl": "https://example.com",
          "identifier": "string",
          "name": "Ava Chen",
          "originsCount": 1,
          "progress": 1,
          "status": "string",
          "totalCalculations": 1
        }
      ],
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com"
      },
      "meta": {
        "currentPage": 1,
        "lastPage": 1,
        "perPage": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Distance matrix jobs. |
| `data[].calculationsCompleted` | number | Completed calculations. |
| `data[].createdAt` | date | Job creation time. |
| `data[].destinationsCount` | number | Number of destination locations. |
| `data[].distanceMode` | string | Distance mode used by the job. |
| `data[].downloadUrl` | string | Download URL when available. |
| `data[].identifier` | string | Public job identifier. |
| `data[].name` | string | Job name. |
| `data[].originsCount` | number | Number of origin locations. |
| `data[].progress` | number | Completion percentage. |
| `data[].status` | string | Job processing status. |
| `data[].totalCalculations` | number | Total calculations in the job. |
| `links.first` | string | First page URL. |
| `links.last` | string | Last page URL. |
| `links.next` | string | Next page URL. |
| `links.prev` | string | Previous page URL. |
| `meta.currentPage` | number | Current page number. |
| `meta.lastPage` | number | Last page number. |
| `meta.perPage` | number | Rows per page. |
| `meta.total` | number | Total rows. |

## Native endpoint

Through the native Geocodio API, this operation is `GET /distance-jobs` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-distance-jobs.md) for the provider-specific parameters and requirements.

