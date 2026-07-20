# Gladia: Update Live Job Debug Params

Updates live job debug parameters in Gladia.

```
PUT https://connect.mindcloud.co/v1/universal/gladia/latest/actions/update-live-job-debug-params
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gladia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gladia/latest/actions/update-live-job-debug-params" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gladia/latest/actions/update-live-job-debug-params', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Gladia live job identifier. |
| `postSessionMetadata` | object | no | Debug metadata object stored in the live job request params after the session ends. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": 1,
      "updated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | number |  |
| `updated` | boolean |  |

## Native endpoint

Through the native Gladia API, this operation is `PATCH /v2/live/:id` (base URL `https://api.gladia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-live-job-debug-params.md) for the provider-specific parameters and requirements.

