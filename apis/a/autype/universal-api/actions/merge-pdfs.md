# Autype: Merge PDFs

Creates a PDF merge job in Autype.

```
POST https://connect.mindcloud.co/v1/universal/autype/latest/actions/merge-pdfs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autype `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/autype/latest/actions/merge-pdfs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/autype/latest/actions/merge-pdfs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileIds[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "id": "string",
      "inputFileIds": [
        "string"
      ],
      "metadata": {},
      "outputFileId": "string",
      "result": {},
      "startedAt": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `completedAt` | date |  |
| `createdAt` | date |  |
| `error` | string |  |
| `id` | string |  |
| `inputFileIds[]` | string |  |
| `metadata` | object |  |
| `outputFileId` | string |  |
| `result` | object |  |
| `startedAt` | date |  |
| `status` | string |  |

## Native endpoint

Through the native Autype API, this operation is `POST /tools/pdf/merge` (base URL `https://api.autype.com/api/v1/dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-pdfs.md) for the provider-specific parameters and requirements.

