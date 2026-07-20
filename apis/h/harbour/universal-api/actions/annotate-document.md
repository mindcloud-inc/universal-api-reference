# Harbour: Annotate Document

Adds annotations to an existing document in Harbour.

```
PUT https://connect.mindcloud.co/v1/universal/harbour/latest/actions/annotate-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harbour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/annotate-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document_id": "string",
  "field_values": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harbour/latest/actions/annotate-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document_id": "string",
    "field_values": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document_id` | string | yes | ID of the document to annotate. |
| `field_values` | object | yes | Map of agreementinput-* field identifiers to annotation payloads, for example { "agreementinput-field": { "value": "Example" } }. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_url": "https://example.com",
      "expires_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_url` | string | Signed URL to download the annotated file. |
| `expires_at` | number | Unix timestamp in milliseconds when the download URL expires. |

## Native endpoint

Through the native Harbour API, this operation is `POST /documents/:document_id/annotate` (base URL `https://api.myharbourshare.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/annotate-document.md) for the provider-specific parameters and requirements.

