# Chargeflow: Create Data Subject Removal Request

Creates a data subject removal request in Chargeflow.

```
POST https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/create-data-subject-removal-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/create-data-subject-removal-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/create-data-subject-removal-request', {
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
      "chargeflow_id": "string",
      "created_at": "string",
      "request_id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chargeflow_id` | string |  |
| `created_at` | string |  |
| `request_id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Chargeflow API, this operation is `POST /data-subject/removal` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-data-subject-removal-request.md) for the provider-specific parameters and requirements.

