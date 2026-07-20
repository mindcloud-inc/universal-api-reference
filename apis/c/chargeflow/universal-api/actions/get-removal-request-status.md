# Chargeflow: Get Removal Request Status

Retrieves a data removal request status from Chargeflow.

```
GET https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-removal-request-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-removal-request-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeflow/latest/actions/get-removal-request-status?${params}`, {
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
| `requestId` | string | yes | The Chargeflow removal request ID. |

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

Through the native Chargeflow API, this operation is `GET /data-subject/removal/{requestId}` (base URL `https://api.chargeflow.io/public/2025-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-removal-request-status.md) for the provider-specific parameters and requirements.

