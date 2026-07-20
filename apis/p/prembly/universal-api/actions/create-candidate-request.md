# Prembly: Create Candidate Request

Creates a candidate request in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/create-candidate-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/create-candidate-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/create-candidate-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_requests": [
        {
          "candidate_email": "ava@example.com",
          "candidate_name": "Ava Chen",
          "reference": "string",
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
| `created_requests[].candidate_email` | string |  |
| `created_requests[].candidate_name` | string |  |
| `created_requests[].reference` | string |  |
| `created_requests[].status` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /api/v1/api/bgc/requests/candidates/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-candidate-request.md) for the provider-specific parameters and requirements.

