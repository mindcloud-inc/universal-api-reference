# Docubee: Replace Document Content

Replaces templated content in a Docubee document.

```
POST https://connect.mindcloud.co/v1/universal/docubee/latest/actions/replace-document-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/replace-document-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docubee/latest/actions/replace-document-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | no | The inline replacement payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | The document ID with replaced content. |

## Native endpoint

Through the native Docubee API, this operation is `POST /contentReplacers` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-document-content.md) for the provider-specific parameters and requirements.

