# PDF Blocks: Add Restrictions

Updates a PDF document with restrictions in PDF Blocks.

```
PUT https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/add-restrictions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF Blocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/add-restrictions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "ownerPassword": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pDFBlocks/latest/actions/add-restrictions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "ownerPassword": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | The input PDF document. |
| `ownerPassword` | string | yes | The password required to open and change permissions of the PDF document. |
| `userPassword` | string | no | The password required to open the PDF document. |
| `encryptionAlgorithm` | string | no | The algorithm used to encrypt the PDF document. |
| `allowCopyContent` | boolean | no | If false, the user cannot copy text and images to the clipboard. |
| `allowChangeContent` | boolean | no | If false, the user cannot change the content of the document. |
| `allowPrint` | boolean | no | If false, the user cannot print the document. |
| `allowPrintHighResolution` | boolean | no | If false, the user cannot print the document in high resolution. |
| `allowCommentAndFillForm` | boolean | no | If false, the user cannot add, edit, or modify annotations or fill form fields. |
| `allowFillForm` | boolean | no | If false, the user cannot fill form fields. |
| `allowAssembleDocument` | boolean | no | If false, the user cannot assemble or manipulate the document. |
| `allowAccessibility` | boolean | no | If false, accessibility programs cannot read the text or images of the document. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PDF Blocks API returns.

## Native endpoint

Through the native PDF Blocks API, this operation is `POST /v1/add_restrictions` (base URL `https://api.pdfblocks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-restrictions.md) for the provider-specific parameters and requirements.

