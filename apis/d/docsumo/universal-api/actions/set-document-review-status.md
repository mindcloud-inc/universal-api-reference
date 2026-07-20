# Docsumo: Set Document Review Status

Updates a document's review status in Docsumo.

```
PUT https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/set-document-review-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docsumo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/set-document-review-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actions": "string",
  "doc_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docsumo/latest/actions/set-document-review-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actions": "string",
    "doc_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actions` | string | yes | Review action path segment. |
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

Through the native Docsumo API, this operation is `POST /api/v1/pik/review/:doc_id/:actions/` (base URL `https://app.docsumo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-document-review-status.md) for the provider-specific parameters and requirements.

