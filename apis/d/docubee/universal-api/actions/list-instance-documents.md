# Docubee: List Instance Documents

Retrieves documents for a Docubee workflow instance.

```
GET https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-instance-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docubee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-instance-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-instance-documents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instanceId` | string | no | The workflow instance ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string | The document ID. |
| `name` | string | The document name. |
| `status` | string | The document status. |

## Native endpoint

Through the native Docubee API, this operation is `GET /instances/:instanceId/documents` (base URL `https://docubee.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-instance-documents.md) for the provider-specific parameters and requirements.

