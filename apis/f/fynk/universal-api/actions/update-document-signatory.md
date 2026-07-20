# fynk: Update Document Signatory

Updates a document signatory in fynk.

```
PUT https://connect.mindcloud.co/v1/universal/fynk/latest/actions/update-document-signatory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a fynk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fynk/latest/actions/update-document-signatory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document": "25c718b2-be8b-44e7-858f-3152e7380022",
  "signatory": "134edea6-de9b-4e48-880e-04b4e77195ff"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fynk/latest/actions/update-document-signatory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document": "25c718b2-be8b-44e7-858f-3152e7380022",
    "signatory": "134edea6-de9b-4e48-880e-04b4e77195ff"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `document` | string | yes | Document UUID. Default: `25c718b2-be8b-44e7-858f-3152e7380022`. |
| `mobile_phone` | string | no | The signatory mobile phone number in E.164 format. Default: `+14155550101`. |
| `signatory` | string | yes | Signatory UUID. Default: `134edea6-de9b-4e48-880e-04b4e77195ff`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native fynk API, this operation is `PUT /documents/:document/signatories/:signatory` (base URL `https://app.fynk.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-signatory.md) for the provider-specific parameters and requirements.

