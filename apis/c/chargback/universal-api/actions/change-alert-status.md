# Chargback: Change Alert Status

Updates an existing alert status in Chargback.

```
PUT https://connect.mindcloud.co/v1/universal/chargback/latest/actions/change-alert-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chargback/latest/actions/change-alert-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "external_id": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chargback/latest/actions/change-alert-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "external_id": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `external_id` | string | yes |  |
| `status` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert_id": "string",
      "message": "string",
      "new_status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert_id` | string | Provider alert identifier for the updated alert. |
| `message` | string | Provider confirmation message for the status update. |
| `new_status` | string | New alert status applied by Chargeback. |

## Native endpoint

Through the native Chargback API, this operation is `PATCH /api/public/v1/alerts/:external_id/` (base URL `https://api.chargeback.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-alert-status.md) for the provider-specific parameters and requirements.

