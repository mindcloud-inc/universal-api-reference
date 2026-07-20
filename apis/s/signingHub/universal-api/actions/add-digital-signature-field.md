# SigningHub: Add Digital Signature Field

Adds a digital signature field in SigningHub.

```
POST https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-digital-signature-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-digital-signature-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": "11191528",
  "documentId": "13459082",
  "order": "1",
  "pageNo": "1",
  "levelOfAssurance": "ELECTRONIC_SIGNATURE",
  "x": "40",
  "y": "100",
  "width": "150",
  "height": "40"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/add-digital-signature-field', {
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
    "levelOfAssurance": "ELECTRONIC_SIGNATURE",
    "x": "40",
    "y": "100",
    "width": "150",
    "height": "40"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | The package ID for which the field is being added. Example: `11191528`. |
| `documentId` | number | yes | The document ID where the field is to be added. Example: `13459082`. |
| `order` | number | yes | Workflow recipient order for the signature field. Example: `1`. |
| `pageNo` | number | yes | Document page number where the field will be added. Example: `1`. |
| `fieldName` | string | no | Optional field name. If omitted, SigningHub assigns one automatically. Example: `Signature 1`. |
| `levelOfAssurance` | string | yes | Signature assurance level, for example ELECTRONIC_SIGNATURE. Default: `ELECTRONIC_SIGNATURE`. Example: `ELECTRONIC_SIGNATURE`. |
| `display` | string | no | Visibility of the field, VISIBLE or INVISIBLE. Default: `VISIBLE`. Example: `VISIBLE`. |
| `x` | number | yes | Left position of the field in pixels. Example: `40`. |
| `y` | number | yes | Top position of the field in pixels. Example: `100`. |
| `width` | number | yes | Field width in pixels. Example: `150`. |
| `height` | number | yes | Field height in pixels. Example: `40`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_on": "2026-05-07T12:00:00.000Z",
      "field_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_on` | date |  |
| `field_name` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `POST /v4/packages/:packageId/documents/:documentId/fields/signature` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-digital-signature-field.md) for the provider-specific parameters and requirements.

