# Eagle Doc: Parse Passport

Creates a passport extraction in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-passport
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-passport" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-passport', {
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
| `file` | file | yes | Passport file to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docType": "string",
      "general": {
        "amendments": "string",
        "checkDigits": "string",
        "dateOfBirth": "2026-05-07T12:00:00.000Z",
        "dateOfExpiry": "2026-05-07T12:00:00.000Z",
        "dateOfIssue": "2026-05-07T12:00:00.000Z",
        "eyeColor": "string",
        "gender": "string",
        "givennames": "Ava Chen",
        "guardianInfo": "string",
        "height": "string",
        "holderSignature": "string",
        "issuingAuthority": "string",
        "issuingCountry": "string",
        "issuingStateCode": "string",
        "machineReadablekey": "string",
        "nationality": "string",
        "nationalityCode": "string",
        "passportNumber": "string",
        "passportType": "string",
        "personalIdNumber": "string",
        "placeOfBirth": "string",
        "residenceAddress": "string",
        "surname": "Ava Chen",
        "visaPages": "string"
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
| `general.amendments` | string |  |
| `general.checkDigits` | string |  |
| `general.dateOfBirth` | date |  |
| `general.dateOfExpiry` | date |  |
| `general.dateOfIssue` | date |  |
| `general.eyeColor` | string |  |
| `general.gender` | string |  |
| `general.givennames` | string |  |
| `general.guardianInfo` | string |  |
| `general.height` | string |  |
| `general.holderSignature` | string |  |
| `general.issuingAuthority` | string |  |
| `general.issuingCountry` | string |  |
| `general.issuingStateCode` | string |  |
| `general.machineReadablekey` | string |  |
| `general.nationality` | string |  |
| `general.nationalityCode` | string |  |
| `general.passportNumber` | string |  |
| `general.passportType` | string |  |
| `general.personalIdNumber` | string |  |
| `general.placeOfBirth` | string |  |
| `general.residenceAddress` | string |  |
| `general.surname` | string |  |
| `general.visaPages` | string |  |
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

Through the native Eagle Doc API, this operation is `POST /api/anydoc/v1/processing` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-passport.md) for the provider-specific parameters and requirements.

