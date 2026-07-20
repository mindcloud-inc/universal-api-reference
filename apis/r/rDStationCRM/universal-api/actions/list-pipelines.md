# RD Station CRM: List Pipelines

Retrieves sales pipelines from RD Station CRM.

```
GET https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/list-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/list-pipelines?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/list-pipelines?${params}`, {
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
        [
          {}
        ]
      ],
      "links": {
        "first": "https://example.com",
        "last": "https://example.com",
        "self": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].createdAt` | string |  |
| `data[].id` | string |  |
| `data[].name` | string |  |
| `data[].order` | number |  |
| `data[].stageIds[]` | array<string> |  |
| `data[].updatedAt` | string |  |
| `links` | object |  |
| `links.first` | string |  |
| `links.last` | string |  |
| `links.self` | string |  |

## Native endpoint

Through the native RD Station CRM API, this operation is `GET /pipelines` (base URL `https://api.rd.services/crm/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pipelines.md) for the provider-specific parameters and requirements.

