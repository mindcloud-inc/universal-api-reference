# Prembly: Get Candidate Request Detail

Retrieves a candidate request from Prembly.

```
GET https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-candidate-request-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-candidate-request-detail?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prembly/latest/actions/get-candidate-request-detail?${params}`, {
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
      "response_submitted": true,
      "status": "string",
      "verification_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidate_email` | string |  |
| `candidate_name` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `package.id` | string |  |
| `package.name` | string |  |
| `payment_status` | string |  |
| `reference` | string |  |
| `response_submitted` | boolean |  |
| `status` | string |  |
| `verification_id` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `GET /requests/candidates/:reference/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-candidate-request-detail.md) for the provider-specific parameters and requirements.

