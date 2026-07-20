# HIPAAtizer: Search Submissions

Finds submissions in HIPAAtizer by workflow and search criteria.

```
GET https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/search-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HIPAAtizer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/search-submissions?connectionId=$CONNECTION_ID&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hIPAAtizer/latest/actions/search-submissions?${params}`, {
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
| `request.searchBy` | string | no | Field used for search. |
| `request.searchFor` | string | no | Search term value. |
| `workflowId` | string | yes | Workflow UUID to scope submission search. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request` | object | no | Optional raw request wrapper. Use `{}` for body when only `workflowId` is provided. |
| `request.additionalColumns` | list<string> | no | Additional columns to include. |
| `request.dates.from` | string | no | Start date filter. |
| `request.dates.to` | string | no | End date filter. |
| `request.includeNotCompleted` | boolean | no | Include incomplete submissions. |
| `request.pagination.limit` | number | no | Pagination page size. |
| `request.pagination.page` | number | no | Pagination page number. |
| `request.searchById` | string | no | ID used for search. |
| `request.sorting.additionalColumn` | string | no | Additional sorting column. |
| `request.sorting.column` | string | no | Primary sorting column. |
| `request.sorting.direction` | string | no | Sort direction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "additionalColumns": {},
        "additionalStatus": "string",
        "comments": 1,
        "createdAt": "string",
        "email": "ava@example.com",
        "id": "string",
        "increment": 1,
        "ipAddress": "string",
        "isArchived": true,
        "status": "string"
      },
      "includeArchived": true,
      "includeNotCompleted": true,
      "pagination": {
        "limit": 1,
        "page": 1,
        "total": 1
      },
      "sorting": {
        "column": "string",
        "direction": "string"
      },
      "title": "string",
      "workflowType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.additionalColumns` | object |  |
| `data.additionalStatus` | string |  |
| `data.comments` | number |  |
| `data.createdAt` | string |  |
| `data.email` | string |  |
| `data.id` | string |  |
| `data.increment` | number |  |
| `data.ipAddress` | string |  |
| `data.isArchived` | boolean |  |
| `data.status` | string |  |
| `includeArchived` | boolean |  |
| `includeNotCompleted` | boolean |  |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.total` | number |  |
| `sorting.column` | string |  |
| `sorting.direction` | string |  |
| `title` | string |  |
| `workflowType` | string |  |

## Native endpoint

Through the native HIPAAtizer API, this operation is `POST /api/v1/api_key/submissions/search` (base URL `https://app.hipaatizer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-submissions.md) for the provider-specific parameters and requirements.

