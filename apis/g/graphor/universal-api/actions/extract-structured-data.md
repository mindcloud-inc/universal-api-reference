# Graphor: Extract Structured Data

Extracts structured data from Graphor documents.

```
POST https://connect.mindcloud.co/v1/universal/graphor/latest/actions/extract-structured-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Graphor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/extract-structured-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileIds": "string",
  "outputSchema": "string",
  "userInstruction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/graphor/latest/actions/extract-structured-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileIds": "string",
    "outputSchema": "string",
    "userInstruction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileIds` | string | yes | Preferred list of file IDs to extract from. |
| `outputSchema` | string | yes | JSON Schema describing the extraction result structure. |
| `thinkingLevel` | string | no | Optional thinking level: fast, balanced, or accurate. |
| `userInstruction` | string | yes | Natural-language instructions that guide the extraction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileIds": [
        "string"
      ],
      "fileNames": [
        "Ava Chen"
      ],
      "rawJson": "string",
      "structuredOutput": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileIds` | array<string> |  |
| `fileNames` | array<string> |  |
| `rawJson` | string |  |
| `structuredOutput` | object |  |

## Native endpoint

Through the native Graphor API, this operation is `POST /run-extraction` (base URL `https://sources.graphorlm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-structured-data.md) for the provider-specific parameters and requirements.

