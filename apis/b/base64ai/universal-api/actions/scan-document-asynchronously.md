# Base64.ai: Scan Document Asynchronously

Starts an asynchronous document scan in Base64.ai.

```
POST https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/scan-document-asynchronously
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Base64.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/scan-document-asynchronously" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/base64ai/latest/actions/scan-document-asynchronously', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the document to scan asynchronously. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asyncFileUUID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asyncFileUUID` | string |  |

## Native endpoint

Through the native Base64.ai API, this operation is `POST /api/scan/async` (base URL `https://base64.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scan-document-asynchronously.md) for the provider-specific parameters and requirements.

