# LOBSTR.IO: Start Run

Starts a new run in LOBSTR.IO.

```
POST https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/start-run
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/start-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "squid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/start-run', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "squid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `squid` | string | yes | The squid hash ID to run. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isDone": true,
      "object": "string",
      "origin": "string",
      "squid": "string",
      "startedAt": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isDone` | boolean |  |
| `object` | string |  |
| `origin` | string |  |
| `squid` | string |  |
| `startedAt` | string |  |
| `status` | string |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `POST /v1/runs` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-run.md) for the provider-specific parameters and requirements.

