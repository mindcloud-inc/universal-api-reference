# Docparser: Fetch Document From URL With Remote ID

Fetches a document from a URL into a Docparser parser and assigns a remote ID.

```
POST https://connect.mindcloud.co/v1/universal/docparser/latest/actions/fetch-document-from-url-with-remote-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/fetch-document-from-url-with-remote-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parserId": "string",
  "url": "https://example.com",
  "remoteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docparser/latest/actions/fetch-document-from-url-with-remote-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parserId": "string",
    "url": "https://example.com",
    "remoteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parserId` | string | yes |  |
| `url` | string | yes |  |
| `remoteId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documentId": "string",
      "message": "string",
      "parserId": "string",
      "remoteId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `documentId` | string |  |
| `message` | string |  |
| `parserId` | string |  |
| `remoteId` | string |  |

## Native endpoint

Through the native Docparser API, this operation is `POST /v2/document/fetch/:PARSER_ID` (base URL `https://api.docparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-document-from-url-with-remote-id.md) for the provider-specific parameters and requirements.

