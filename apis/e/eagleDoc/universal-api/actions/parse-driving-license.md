# Eagle Doc: Parse Driving License

Creates a driving license extraction in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-driving-license
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-driving-license" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-driving-license', {
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
| `file` | file | yes | Driving license file to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docType": "string",
      "general": {
        "address": "string",
        "class": "string",
        "country": "string",
        "dob": "2026-05-07T12:00:00.000Z",
        "endorsements": "string",
        "expirationDate": "2026-05-07T12:00:00.000Z",
        "eyeColor": "string",
        "fullName": "Ava Chen",
        "hairColor": "string",
        "height": "string",
        "issueDate": "2026-05-07T12:00:00.000Z",
        "issuingAuthority": "string",
        "licenseNumber": "string",
        "photo": "string",
        "restrictions": "string",
        "signature": "string",
        "state": "string",
        "weight": "string",
        "zipCode": "string"
      },
      "processingInfo": {
        "docConfigId": {},
        "docType": "string",
        "duration": "string",
        "fileHash": "string",
        "language": "string",
        "numberOfPages": "string",
        "version": "string"
      },
      "signatures": {},
      "verification": {
        "nonDuplication": {
          "flagValid": true,
          "message": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docType` | string |  |
| `general.address` | string |  |
| `general.class` | string |  |
| `general.country` | string |  |
| `general.dob` | date |  |
| `general.endorsements` | string |  |
| `general.expirationDate` | date |  |
| `general.eyeColor` | string |  |
| `general.fullName` | string |  |
| `general.hairColor` | string |  |
| `general.height` | string |  |
| `general.issueDate` | date |  |
| `general.issuingAuthority` | string |  |
| `general.licenseNumber` | string |  |
| `general.photo` | string |  |
| `general.restrictions` | string |  |
| `general.signature` | string |  |
| `general.state` | string |  |
| `general.weight` | string |  |
| `general.zipCode` | string |  |
| `processingInfo.docConfigId` | object |  |
| `processingInfo.docType` | string |  |
| `processingInfo.duration` | string |  |
| `processingInfo.fileHash` | string |  |
| `processingInfo.language` | string |  |
| `processingInfo.numberOfPages` | string |  |
| `processingInfo.version` | string |  |
| `signatures` | object |  |
| `verification.nonDuplication.flagValid` | boolean |  |
| `verification.nonDuplication.message` | string |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `POST /api/anydoc/v1/processing` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-driving-license.md) for the provider-specific parameters and requirements.

