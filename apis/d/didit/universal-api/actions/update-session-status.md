# Didit: Update Session Status

Updates a session status in Didit.

```
PUT https://connect.mindcloud.co/v1/universal/didit/latest/actions/update-session-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Didit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/didit/latest/actions/update-session-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/didit/latest/actions/update-session-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Didit session identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sessionId": "string",
      "status": "string",
      "vendorData": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sessionId` | string |  |
| `status` | string |  |
| `vendorData` | string |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Didit API, this operation is `PATCH https://verification.didit.me/v3/session/{sessionId}/update-status/` (base URL `https://verification.didit.me/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-session-status.md) for the provider-specific parameters and requirements.

