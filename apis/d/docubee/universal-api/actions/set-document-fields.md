# Docubee: Set Document Fields

Sets fields on a document in Docubee.

```
PUT https://connect.mindcloud.co/v1/universal/docubee/latest/actions/set-document-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/set-document-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docubee/latest/actions/set-document-fields', {
  method: 'PUT',
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
| `body` | string | no | The fields configuration payload. |
| `documentId` | string | no | The Docubee document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | The document ID whose fields were configured. |
| `success` | boolean | Whether the field configuration was accepted. |

## Native endpoint

Through the native Docubee API, this operation is `PUT /documents/:documentId/fields` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-document-fields.md) for the provider-specific parameters and requirements.

