# Transloadit: Create Assembly

Creates a new assembly in Transloadit.

```
POST https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/create-assembly
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Transloadit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/create-assembly" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "params": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/transloadit/latest/actions/create-assembly', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "params": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `params` | string | yes | JSON string containing the Transloadit Assembly instructions, including steps and optional fields such as auth, template_id, notify_url, and signatures when applicable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assembly_id": "string",
      "assembly_ssl_url": "https://example.com",
      "message": "string",
      "ok": "string",
      "results": {},
      "uploads": [
        {}
      ],
      "websocket_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assembly_id` | string | Created assembly ID. |
| `assembly_ssl_url` | string | Secure URL of the created assembly. |
| `message` | string | Human-readable result message. |
| `ok` | string | Status code returned by Transloadit for assembly creation. |
| `results` | object | Assembly results grouped by step. |
| `uploads` | array<object> | Uploads attached to the assembly. |
| `websocket_url` | string | WebSocket URL for assembly updates. |

## Native endpoint

Through the native Transloadit API, this operation is `POST /assemblies` (base URL `https://api2.transloadit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-assembly.md) for the provider-specific parameters and requirements.

