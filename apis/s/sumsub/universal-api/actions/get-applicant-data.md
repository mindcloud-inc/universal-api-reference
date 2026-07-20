# Sumsub: Get Applicant Data



```
GET https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/get-applicant-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumsub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/get-applicant-data?connectionId=$CONNECTION_ID&applicantId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "applicantId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumsub/latest/actions/get-applicant-data?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `applicantId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicantPlatform": "string",
      "clientId": "string",
      "createdAt": "string",
      "createdBy": "string",
      "externalUserId": "string",
      "id": "string",
      "inspectionId": "string",
      "key": "string",
      "notes": [
        {
          "clientEntry": true,
          "createdAt": "string",
          "moderatorName": "Ava Chen",
          "note": "string"
        }
      ],
      "requiredIdDocs": {
        "docSets": [
          {
            "idDocSetType": "string",
            "types": [
              "string"
            ],
            "videoRequired": "string"
          }
        ]
      },
      "review": {
        "attemptCnt": 1,
        "attemptId": "string",
        "createDate": "string",
        "levelAutoCheckMode": {},
        "levelName": "Ava Chen",
        "priority": 1,
        "reviewId": "string",
        "reviewStatus": "string"
      },
      "tags": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicantPlatform` | string |  |
| `clientId` | string |  |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `externalUserId` | string |  |
| `id` | string |  |
| `inspectionId` | string |  |
| `key` | string |  |
| `notes[].clientEntry` | boolean |  |
| `notes[].createdAt` | string |  |
| `notes[].moderatorName` | string |  |
| `notes[].note` | string |  |
| `requiredIdDocs.docSets[].idDocSetType` | string |  |
| `requiredIdDocs.docSets[].types[]` | string |  |
| `requiredIdDocs.docSets[].videoRequired` | string |  |
| `review.attemptCnt` | number |  |
| `review.attemptId` | string |  |
| `review.createDate` | string |  |
| `review.levelAutoCheckMode` | object |  |
| `review.levelName` | string |  |
| `review.priority` | number |  |
| `review.reviewId` | string |  |
| `review.reviewStatus` | string |  |
| `tags[]` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Sumsub API, this operation is `GET /resources/applicants/:applicantId/one` (base URL `https://api.sumsub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-applicant-data.md) for the provider-specific parameters and requirements.

