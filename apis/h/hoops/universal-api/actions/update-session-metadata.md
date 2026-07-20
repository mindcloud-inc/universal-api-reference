# Hoops: Update Session Metadata



```
PUT https://connect.mindcloud.co/v1/universal/hoops/latest/actions/update-session-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hoops `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hoops/latest/actions/update-session-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hoops/latest/actions/update-session-metadata', {
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
| `sessionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "metadata": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `metadata` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Hoops API, this operation is `PATCH /sessions/{session_id}/metadata` (base URL `https://use.hoop.dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-session-metadata.md) for the provider-specific parameters and requirements.

