# Docparser: Upload Document By Content With Remote ID

Uploads document content to a Docparser parser and assigns a remote ID.

```
POST https://connect.mindcloud.co/v1/universal/docparser/latest/actions/upload-document-by-content-with-remote-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docparser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/upload-document-by-content-with-remote-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parserId": "string",
  "fileContent": "string",
  "fileName": "Ava Chen",
  "remoteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docparser/latest/actions/upload-document-by-content-with-remote-id', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parserId": "string",
    "fileContent": "string",
    "fileName": "Ava Chen",
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
| `fileContent` | string | yes |  |
| `fileName` | string | yes |  |
| `remoteId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "fileSize": 1,
      "id": "string",
      "pages": 1,
      "quotaGranted": "string",
      "quotaLeft": 1,
      "quotaRefill": "string",
      "quotaUsed": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string |  |
| `fileSize` | number |  |
| `id` | string |  |
| `pages` | number |  |
| `quotaGranted` | string |  |
| `quotaLeft` | number |  |
| `quotaRefill` | string |  |
| `quotaUsed` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Docparser API, this operation is `POST /v1/document/upload/:PARSER_ID` (base URL `https://api.docparser.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-document-by-content-with-remote-id.md) for the provider-specific parameters and requirements.

