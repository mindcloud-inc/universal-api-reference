# xMatters: Get import jobs

Retrieves import jobs from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-import-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-import-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-import-jobs?${params}`, {
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
      "count": 1,
      "data": [
        {
          "by": {
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "links": {
              "self": "https://example.com"
            },
            "recipientType": "string",
            "targetName": "Ava Chen"
          },
          "finishedAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "links": {
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "processedCount": 1,
          "processingAt": "2026-05-07T12:00:00.000Z",
          "started": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "totalCount": 1,
          "transform": {
            "name": "Ava Chen",
            "url": "https://example.com"
          }
        }
      ],
      "links": {
        "self": "https://example.com"
      },
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].by.firstName` | string |  |
| `data[].by.id` | string |  |
| `data[].by.lastName` | string |  |
| `data[].by.links.self` | string |  |
| `data[].by.recipientType` | string |  |
| `data[].by.targetName` | string |  |
| `data[].finishedAt` | date |  |
| `data[].id` | string |  |
| `data[].links.self` | string |  |
| `data[].name` | string |  |
| `data[].processedCount` | number |  |
| `data[].processingAt` | date |  |
| `data[].started` | date |  |
| `data[].status` | string |  |
| `data[].totalCount` | number |  |
| `data[].transform.name` | string |  |
| `data[].transform.url` | string |  |
| `links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET imports` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-import-jobs.md) for the provider-specific parameters and requirements.

