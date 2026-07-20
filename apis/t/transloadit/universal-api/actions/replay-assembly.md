# Transloadit: Replay Assembly

Replays an existing assembly in Transloadit.

```
POST https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/replay-assembly
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/replay-assembly" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assemblyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/replay-assembly', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assemblyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assemblyId` | string | yes | The ID of the assembly to replay. |
| `params` | string | no | Optional JSON string containing replay parameters supported by Transloadit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assembly_id": "string",
      "assembly_ssl_url": "https://example.com",
      "error": "string",
      "message": "string",
      "ok": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assembly_id` | string | Unique Transloadit assembly identifier. |
| `assembly_ssl_url` | string | Secure URL for the replayed assembly resource. |
| `error` | string | Error description when replay fails. |
| `message` | string | Human-readable result message from Transloadit. |
| `ok` | string | Status text for the assembly replay request. |

## Native endpoint

Through the native Transloadit API, this operation is `POST /assemblies/:assemblyId/replay` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replay-assembly.md) for the provider-specific parameters and requirements.

