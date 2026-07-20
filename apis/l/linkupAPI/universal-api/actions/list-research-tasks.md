# LinkupAPI: List Research Tasks

Retrieves a list of research tasks from LinkupAPI.

```
GET https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/list-research-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkupAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/list-research-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkupAPI/latest/actions/list-research-tasks?${params}`, {
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
      "metadata": {
        "page": 1,
        "pageSize": 1,
        "total": 1,
        "totalPages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> | Research tasks returned by Linkup. |
| `data[].createdAt` | date | When the research task was created. |
| `data[].error` | string | The error message when the task fails. |
| `data[].id` | string | The research task ID. |
| `data[].input` | object | The input used to create the research task. |
| `data[].output` | object | The research task output when completed. |
| `data[].status` | string | The research task status. |
| `data[].updatedAt` | date | When the research task was last updated. |
| `metadata.page` | number | The current page number. |
| `metadata.pageSize` | number | The number of tasks per page. |
| `metadata.total` | number | The total number of research tasks. |
| `metadata.totalPages` | number | The total number of pages. |

## Native endpoint

Through the native LinkupAPI API, this operation is `GET /research` (base URL `https://api.linkup.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-research-tasks.md) for the provider-specific parameters and requirements.

