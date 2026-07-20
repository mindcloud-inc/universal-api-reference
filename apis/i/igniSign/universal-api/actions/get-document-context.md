# IgniSign: Get Document Context



```
GET https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-document-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-document-context?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/get-document-context?${params}`, {
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
| `documentId` | string | yes | The IgniSign document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "label": "string",
      "signatureRequestId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `label` | string |  |
| `signatureRequestId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native IgniSign API, this operation is `GET /v4/documents/:documentId/context` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-context.md) for the provider-specific parameters and requirements.

