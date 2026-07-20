# iubenda: Create Document

Creates a document in iubenda.

```
POST https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iubenda `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "Select a file under 1MB"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "Select a file under 1MB"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Document file to upload. Max 1MB. Example: `Select a file under 1MB`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "mime_type": "string",
      "name": "Ava Chen",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `mime_type` | string |  |
| `name` | string |  |
| `timestamp` | string |  |

## Native endpoint

Through the native iubenda API, this operation is `POST /beta/documents` (base URL `https://consent.iubenda.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

