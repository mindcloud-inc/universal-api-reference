# SigningHub: Add Text Box Field

Adds a text box field in SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-text-box-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-text-box-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "11191528",
  "documentId": "13459082",
  "order": "1",
  "pageNo": "1",
  "type": "TEXT",
  "fieldType": "Text",
  "maxLength": "100",
  "fontName": "HELVETICA",
  "fontSize": "12",
  "x": "40",
  "y": "180",
  "width": "180",
  "height": "24"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-text-box-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": "11191528",
    "documentId": "13459082",
    "order": "1",
    "pageNo": "1",
    "type": "TEXT",
    "fieldType": "Text",
    "maxLength": "100",
    "fontName": "HELVETICA",
    "fontSize": "12",
    "x": "40",
    "y": "180",
    "width": "180",
    "height": "24"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | Package ID to which the document is added. Example: `11191528`. |
| `documentId` | number | yes | The document ID where the text field is to be added. Example: `13459082`. |
| `order` | number | yes | Workflow recipient order for the text field. Example: `1`. |
| `pageNo` | number | yes | Document page number where the field will be added. Example: `1`. |
| `fieldName` | string | no | Optional text field name. Example: `Text 1`. |
| `type` | string | yes | Text box type, for example TEXT or DATE. Default: `TEXT`. Example: `TEXT`. |
| `fieldType` | string | yes | Field type, Text or Number. Default: `Text`. Example: `Text`. |
| `maxLength` | number | yes | Maximum allowed text length, between 1 and 9999. Default: `100`. Example: `100`. |
| `placeholder` | string | no | Placeholder text shown in the text field. Example: `Enter text`. |
| `fontName` | string | yes | Font name, for example HELVETICA. Default: `HELVETICA`. Example: `HELVETICA`. |
| `fontSize` | string | yes | Font size, for example 12. Default: `12`. Example: `12`. |
| `x` | number | yes | Left position of the field in pixels. Example: `40`. |
| `y` | number | yes | Top position of the field in pixels. Example: `180`. |
| `width` | number | yes | Field width in pixels. Example: `180`. |
| `height` | number | yes | Field height in pixels. Example: `24`. |
| `multiline` | boolean | no | Set true to create a multiline text area. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field_name` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/:packageId/documents/:documentId/fields/text` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-text-box-field.md) for the provider-specific parameters and requirements.

