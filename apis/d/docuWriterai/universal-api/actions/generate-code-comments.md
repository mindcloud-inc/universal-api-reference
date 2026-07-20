# DocuWriter.ai: Generate Code Comments



```
POST https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/generate-code-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuWriter.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/generate-code-comments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sourceCode": "string",
  "filename": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuWriterai/latest/actions/generate-code-comments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sourceCode": "string",
    "filename": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sourceCode` | string | yes | Raw source code to comment. |
| `filename` | string | yes | Name of the source file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "generation": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string | Filename returned for the commented output. |
| `generation` | string | Generated commented code output. |

## Native endpoint

Through the native DocuWriter.ai API, this operation is `POST /api/generate-code-comments` (base URL `https://app.docuwriter.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-code-comments.md) for the provider-specific parameters and requirements.

