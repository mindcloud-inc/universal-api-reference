# Middesk: Get a document

Retrieves a document from your Middesk account.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-document?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/get-document?${params}`, {
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
| `id` | string | yes | ID of the document to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdAt": "string",
      "documentType": "string",
      "downloadUrl": "https://example.com",
      "filename": "Ava Chen",
      "filingDate": "string",
      "id": "string",
      "metadata": {},
      "object": "string",
      "size": 1,
      "source": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string |  |
| `createdAt` | string |  |
| `documentType` | string |  |
| `downloadUrl` | string |  |
| `filename` | string |  |
| `filingDate` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `size` | number |  |
| `source` | object |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /documents/:id` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

