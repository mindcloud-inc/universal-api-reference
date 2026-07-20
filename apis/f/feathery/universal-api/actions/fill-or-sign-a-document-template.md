# Feathery: Fill or Sign a Document Template



```
POST https://connect.mindcloud.co/v1/universal/feathery/latest/actions/fill-or-sign-a-document-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/fill-or-sign-a-document-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/feathery/latest/actions/fill-or-sign-a-document-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | string | yes | The ID of the document to fill. |
| `field_values` | object | no | A mapping of document field IDs to values. |
| `signer_email` | string | no | Email address to route the document to for signature after filling. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user_id` | string | no | Associate an existing Feathery user with the generated document. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file_url` | string |  |

## Native endpoint

Through the native Feathery API, this operation is `POST /api/document/fill/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fill-or-sign-a-document-template.md) for the provider-specific parameters and requirements.

