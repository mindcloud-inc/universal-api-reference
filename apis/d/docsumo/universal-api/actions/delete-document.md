# Docsumo: Delete Document

Deletes an existing document from Docsumo.

```
DELETE https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docsumo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/delete-document?connectionId=$CONNECTION_ID&doc_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "doc_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/delete-document?${params}`, {
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
| `doc_id` | string | yes | Docsumo document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": "string",
      "error_code": "string",
      "message": "string",
      "source": "string",
      "status": "string",
      "status_code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `error` | string |  |
| `error_code` | string |  |
| `message` | string |  |
| `source` | string |  |
| `status` | string |  |
| `status_code` | number |  |

## Native endpoint

Through the native Docsumo API, this operation is `DELETE /api/v1/eevee/apikey/delete/:doc_id/` (base URL `https://app.docsumo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.

