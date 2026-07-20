# LOBSTR.IO: Upload Tasks

Uploads tasks to LOBSTR.IO from a file.

```
POST https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/upload-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/upload-tasks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "squid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/upload-tasks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "squid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The CSV or TSV file containing task data. |
| `squid` | string | yes | The squid hash ID to add tasks to. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `object` | string |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `POST /v1/tasks/upload` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-tasks.md) for the provider-specific parameters and requirements.

