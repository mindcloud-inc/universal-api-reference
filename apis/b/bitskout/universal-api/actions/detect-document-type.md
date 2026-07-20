# Bitskout: Detect Document Type

Detects a document type with Bitskout.

```
POST https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/detect-document-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitskout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/detect-document-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "doctype": "legal"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/detect-document-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "doctype": "legal"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `doctype` | list<string> | yes | Document type category to detect. One of: `legal`, `logistics`. |
| `fileUrl` | string | no | Direct download URL for the document to classify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": {
        "Document Type": "string",
        "RawJSON": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | object | Document type detection outputs |
| `outputs.Document Type` | string | Document Type |
| `outputs.RawJSON` | string | Raw JSON |

## Native endpoint

Through the native Bitskout API, this operation is `POST /actions/doctype_:doctype` (base URL `https://api.bitskout.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-document-type.md) for the provider-specific parameters and requirements.

