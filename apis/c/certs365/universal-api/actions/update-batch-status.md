# Certs 365: Update Batch Status

Updates batch certificate statuses in Certs 365.

```
PUT https://connect.mindcloud.co/v1/universal/certs365/latest/actions/update-batch-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Certs 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/update-batch-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "batch": 1,
  "status": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/certs365/latest/actions/update-batch-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "batch": 1,
    "status": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Issuer email. |
| `batch` | number | yes | Certificate batch number. |
| `status` | number | yes | Batch status value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | object |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Certs 365 API, this operation is `POST /api/update-batch-status` (base URL `https://api1.certs365.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-batch-status.md) for the provider-specific parameters and requirements.

