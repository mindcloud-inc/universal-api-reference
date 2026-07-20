# DirectIQ: Get bounce report

Retrieves campaign bounce records from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-bounce-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-bounce-report?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-bounce-report?${params}`, {
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
      "result": [
        [
          {}
        ]
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result[]` | array<object> |  |
| `result[].bounceType` | string |  |
| `result[].createdDate` | date |  |
| `result[].createdDateOffset` | date |  |
| `result[].createdDateString` | string |  |
| `result[].email` | string |  |
| `result[].enumBounceType` | number |  |
| `result[].firstName` | string |  |
| `result[].id` | number |  |
| `result[].lastName` | string |  |
| `result[].status` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /core/reports/bounces` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-bounce-report.md) for the provider-specific parameters and requirements.

