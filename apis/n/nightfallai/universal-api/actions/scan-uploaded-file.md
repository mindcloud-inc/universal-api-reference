# Nightfall.ai: Scan Uploaded File

Scans an uploaded file with Nightfall.ai.

```
POST https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/scan-uploaded-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/scan-uploaded-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string",
  "policy": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/scan-uploaded-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string",
    "policy": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | The upload UUID to scan. |
| `policy` | object | yes | Nightfall policy object with webhookURL plus detection rules or detection rule UUIDs. |
| `requestMetadata` | string | no | Optional metadata echoed back when the asynchronous scan completes. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nightfall.ai API returns.

## Native endpoint

Through the native Nightfall.ai API, this operation is `POST /v3/upload/:fileId/scan` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scan-uploaded-file.md) for the provider-specific parameters and requirements.

