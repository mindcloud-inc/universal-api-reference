# Smartcat: Request Document Export

Creates a document export task in Smartcat.

```
POST https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/request-document-export
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/request-document-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentIds": "abc_9,a02_9"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartcat/latest/actions/request-document-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentIds": "abc_9,a02_9"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentIds` | string | yes | One or more document IDs in documentId_targetLanguageId format Accepts multiple values in one string, delimited by `,`. Example: `abc_9,a02_9`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no | Export type, such as target Example: `target`. |
| `stageNumber` | number | no | Workflow stage number to export from Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentIds": [
        "string"
      ],
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentIds` | array<string> |  |
| `id` | string |  |

## Native endpoint

Through the native Smartcat API, this operation is `POST /api/integration/v1/document/export` (base URL `https://smartcat.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-document-export.md) for the provider-specific parameters and requirements.

