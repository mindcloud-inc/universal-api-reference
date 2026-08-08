# XOi: List Jobs



```
GET https://connect.mindcloud.co/v1/universal/xOi/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xOi/latest/actions/list-jobs?${params}`, {
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
      "assigneeIds": [
        "string"
      ],
      "createdAt": "string",
      "customerName": "Ava Chen",
      "id": "string",
      "jobLocation": "string",
      "workOrderNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigneeIds` | array<string> |  |
| `createdAt` | string |  |
| `customerName` | string |  |
| `id` | string |  |
| `jobLocation` | string |  |
| `workOrderNumber` | string |  |

## Native endpoint

Through the native XOi API, this operation is `POST https://gql-jobs-external.xoi.io/graphql` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

