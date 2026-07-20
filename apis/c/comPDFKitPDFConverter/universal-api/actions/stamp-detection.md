# ComPDFKit PDF Converter: Stamp Detection

Creates stamp detection output from a document.

```
POST https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/stamp-detection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ComPDFKit PDF Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/stamp-detection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/stamp-detection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {},
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data` | object |  |
| `msg` | string |  |

## Native endpoint

Through the native ComPDFKit PDF Converter API, this operation is `POST /v2/process/documentAI/detectionStamp` (base URL `https://api-server.compdf.com/server`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stamp-detection.md) for the provider-specific parameters and requirements.

