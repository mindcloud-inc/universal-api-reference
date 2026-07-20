# Eagle Doc: Parse Resume

Creates a resume extraction in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-resume
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-resume" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-resume', {
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
| `file` | file | yes | Resume file to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docType": "string",
      "general": {
        "address": "string",
        "city": "string",
        "country": "string",
        "email": "ava@example.com",
        "fullName": "Ava Chen",
        "gitHub": "string",
        "hobbies": "string",
        "linkedIn": "https://example.com",
        "objective": "string",
        "phone": "string",
        "programmingLanguages": [
          "string"
        ],
        "state": "string",
        "street": "string",
        "summary": "string",
        "url": "https://example.com",
        "zip": "string"
      },
      "lists": {
        "certificationList": [
          {
            "date": "2026-05-07T12:00:00.000Z",
            "institution": "string",
            "title": "string"
          }
        ],
        "educationList": [
          {
            "city": "string",
            "country": "string",
            "degreeName": "Ava Chen",
            "description": "string",
            "endDate": "2026-05-07T12:00:00.000Z",
            "gpa": {},
            "honors": {},
            "institutionName": "Ava Chen",
            "majors": {},
            "minors": {},
            "startDate": "2026-05-07T12:00:00.000Z",
            "state": {}
          }
        ],
        "workExperienceList": [
          {
            "city": "string",
            "country": {},
            "description": "string",
            "employer": "string",
            "endDate": "2026-05-07T12:00:00.000Z",
            "jobTitle": "string",
            "startDate": "2026-05-07T12:00:00.000Z",
            "state": "string"
          }
        ]
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
| `general.city` | string |  |
| `general.country` | string |  |
| `general.email` | string |  |
| `general.fullName` | string |  |
| `general.gitHub` | string |  |
| `general.hobbies` | string |  |
| `general.linkedIn` | string |  |
| `general.objective` | string |  |
| `general.phone` | string |  |
| `general.programmingLanguages[]` | string |  |
| `general.state` | string |  |
| `general.street` | string |  |
| `general.summary` | string |  |
| `general.url` | string |  |
| `general.zip` | string |  |
| `lists.certificationList[].date` | date |  |
| `lists.certificationList[].institution` | string |  |
| `lists.certificationList[].title` | string |  |
| `lists.educationList[].city` | string |  |
| `lists.educationList[].country` | string |  |
| `lists.educationList[].degreeName` | string |  |
| `lists.educationList[].description` | string |  |
| `lists.educationList[].endDate` | date |  |
| `lists.educationList[].gpa` | object |  |
| `lists.educationList[].honors` | object |  |
| `lists.educationList[].institutionName` | string |  |
| `lists.educationList[].majors` | object |  |
| `lists.educationList[].minors` | object |  |
| `lists.educationList[].startDate` | date |  |
| `lists.educationList[].state` | object |  |
| `lists.workExperienceList[].city` | string |  |
| `lists.workExperienceList[].country` | object |  |
| `lists.workExperienceList[].description` | string |  |
| `lists.workExperienceList[].employer` | string |  |
| `lists.workExperienceList[].endDate` | date |  |
| `lists.workExperienceList[].jobTitle` | string |  |
| `lists.workExperienceList[].startDate` | date |  |
| `lists.workExperienceList[].state` | string |  |
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

Through the native Eagle Doc API, this operation is `POST /api/anydoc/v1/processing` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-resume.md) for the provider-specific parameters and requirements.

