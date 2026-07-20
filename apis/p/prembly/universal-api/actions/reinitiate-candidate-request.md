# Prembly: Reinitiate Candidate Request

Reinitiates a candidate request in Prembly.

```
PUT https://connect.mindcloud.co/v1/universal/prembly/latest/actions/reinitiate-candidate-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/reinitiate-candidate-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/reinitiate-candidate-request', {
  method: 'PUT',
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
      "candidate_email": "ava@example.com",
      "reference": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `candidate_email` | string |  |
| `reference` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /candidates/:reference/reinitiate/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reinitiate-candidate-request.md) for the provider-specific parameters and requirements.

