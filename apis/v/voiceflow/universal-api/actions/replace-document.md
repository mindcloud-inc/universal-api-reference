# Voiceflow: Replace Document

Replaces a knowledge base document in Voiceflow.

```
PUT https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/replace-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/replace-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "69c5818ee08900f39366946a",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/replace-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "69c5818ee08900f39366946a",
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | ID of the document to target. Example: `69c5818ee08900f39366946a`. |
| `data` | object | yes | Replacement document payload nested under the top-level data field. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxChunkSize` | number | no | Optional chunk size in tokens. Example: `1000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "data": {
          "name": "Ava Chen",
          "refreshRate": "string",
          "type": "string",
          "url": "https://example.com"
        },
        "documentID": "string",
        "status": {
          "type": "string"
        },
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.data.name` | string | Display name for the document. |
| `data.data.refreshRate` | string | Configured refresh cadence for the document. |
| `data.data.type` | string | Document source type. |
| `data.data.url` | string | Source URL for the document. |
| `data.documentID` | string | ID of the replaced document. |
| `data.status.type` | string | Current indexing status for the document. |
| `data.updatedAt` | date | When the document was updated. |

## Native endpoint

Through the native Voiceflow API, this operation is `PUT https://realtime-api.voiceflow.com/v1alpha1/public/knowledge-base/document/:documentId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-document.md) for the provider-specific parameters and requirements.

