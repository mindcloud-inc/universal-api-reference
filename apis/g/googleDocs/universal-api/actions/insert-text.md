# Google Docs: Insert Text

Inserts text into a Google Docs document.

```
PUT https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/insert-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Docs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/insert-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "locationIndex": 1,
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleDocs/latest/actions/insert-text', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "locationIndex": 1,
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | list<string> | yes | ID of the document to update |
| `locationIndex` | number | yes | Index position where text should be inserted |
| `text` | string | yes | Text to insert |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "writeControl": {
        "requiredRevisionId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string |  |
| `writeControl.requiredRevisionId` | string |  |

## Native endpoint

Through the native Google Docs API, this operation is `POST /[:documentId]\:batchUpdate` (base URL `https://docs.googleapis.com/v1/documents`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-text.md) for the provider-specific parameters and requirements.

