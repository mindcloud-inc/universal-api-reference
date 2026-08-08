# XOi: List Jobs by Date Range



```
GET https://connect.mindcloud.co/v1/universal/xOi/latest/actions/list-jobs-by-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XOi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xOi/latest/actions/list-jobs-by-date-range?connectionId=$CONNECTION_ID&limit=25&offset=0&dateType=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "dateType": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xOi/latest/actions/list-jobs-by-date-range?${params}`, {
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
| `dateType` | string | yes | One of: `0`, `1`. |
| `gte` | date | no |  |
| `lte` | date | no |  |
| `ascending` | boolean | no | Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigneeIds": [
        "string"
      ],
      "completedAt": "string",
      "createdAt": "string",
      "customerEmail": "ava@example.com",
      "customerName": "Ava Chen",
      "externalId": "string",
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
| `completedAt` | string |  |
| `createdAt` | string |  |
| `customerEmail` | string |  |
| `customerName` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `jobLocation` | string |  |
| `workOrderNumber` | string |  |

## Native endpoint

Through the native XOi API, this operation is `POST https://gql-jobs-external.xoi.io/graphql` (base URL `https://gql-jobs-external.xoi.io/graphql`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs-by-date-range.md) for the provider-specific parameters and requirements.

