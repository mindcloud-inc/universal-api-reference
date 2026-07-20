# Eagle Doc: Extract Signatures

Creates a signature extraction in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/extract-signatures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/extract-signatures" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/extract-signatures', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Document file that contains signatures |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileHash": "string",
      "numberOfPages": 1,
      "signatures": [
        {
          "binary": "string",
          "boundingBox": [
            1
          ],
          "confidence": 1,
          "hasSignatureLabelsNearby": true,
          "hasVisibleBoxSurrounding": true,
          "image": "string",
          "numberOfSignaturesExpected": 1,
          "page": 1,
          "signatureColor": [
            1
          ]
        }
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileHash` | string |  |
| `numberOfPages` | number |  |
| `signatures[].binary` | string |  |
| `signatures[].boundingBox[]` | number |  |
| `signatures[].confidence` | number |  |
| `signatures[].hasSignatureLabelsNearby` | boolean |  |
| `signatures[].hasVisibleBoxSurrounding` | boolean |  |
| `signatures[].image` | string |  |
| `signatures[].numberOfSignaturesExpected` | number |  |
| `signatures[].page` | number |  |
| `signatures[].signatureColor[]` | number |  |
| `version` | string |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `POST /api/signature/v1/extract` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-signatures.md) for the provider-specific parameters and requirements.

