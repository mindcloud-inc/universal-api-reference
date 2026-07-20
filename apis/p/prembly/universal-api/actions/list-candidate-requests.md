# Prembly: List Candidate Requests

Retrieves candidate requests from Prembly.

```
GET https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-candidate-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-candidate-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prembly/latest/actions/list-candidate-requests?${params}`, {
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
      "pagination": {
        "has_next": true,
        "has_previous": true,
        "page": 1,
        "page_size": 1,
        "total_pages": 1,
        "total_records": 1
      },
      "results": [
        {
          "candidate_email": "ava@example.com",
          "candidate_name": "Ava Chen",
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "package": {
            "id": "string",
            "name": "Ava Chen"
          },
          "payment_status": "string",
          "reference": "string",
          "service_type": "string",
          "status": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.has_next` | boolean |  |
| `pagination.has_previous` | boolean |  |
| `pagination.page` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total_pages` | number |  |
| `pagination.total_records` | number |  |
| `results[].candidate_email` | string |  |
| `results[].candidate_name` | string |  |
| `results[].created_at` | date |  |
| `results[].id` | string |  |
| `results[].package.id` | string |  |
| `results[].package.name` | string |  |
| `results[].payment_status` | string |  |
| `results[].reference` | string |  |
| `results[].service_type` | string |  |
| `results[].status` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `GET /api/v1/api/bgc/requests/candidates/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-candidate-requests.md) for the provider-specific parameters and requirements.

