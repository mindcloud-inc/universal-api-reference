# HRBLADE: Get Response



```
GET https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HRBLADE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-response?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-response?${params}`, {
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
| `id` | number | yes | Response identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "error": true,
      "response": {
        "data": {
          "agencyId": 1,
          "blocked": 1,
          "companyId": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "full": "string",
          "id": 1,
          "invited": 1,
          "job": {
            "active": 1,
            "agencyId": 1,
            "askCv": 1,
            "askMotivationLetter": 1,
            "blockTry": 1,
            "company": {
              "agencyId": 1,
              "createdAt": "2026-05-07T12:00:00.000Z",
              "id": 1,
              "logo": "string",
              "name": "Ava Chen",
              "permissions": {
                "createJobs": true,
                "createRooms": true,
                "editCompany": true,
                "viewJobs": true,
                "viewRooms": true
              },
              "updatedAt": "2026-05-07T12:00:00.000Z"
            },
            "companyId": 1,
            "createdAt": "2026-05-07T12:00:00.000Z",
            "description": "string",
            "forFollowUp": 1,
            "hashLink": "https://example.com",
            "id": 1,
            "interviewedCount": 1,
            "invitedCount": 1,
            "language": "string",
            "name": "Ava Chen",
            "permissions": {
              "editJobs": true,
              "rateResponses": true
            },
            "previewVideo": "string",
            "randomOrder": 1,
            "startAt": "2026-05-07T12:00:00.000Z",
            "updatedAt": "2026-05-07T12:00:00.000Z"
          },
          "jobId": 1,
          "language": "string",
          "overallCompatibility": 1,
          "permissions": {
            "rateResponses": true
          },
          "pipelineIndex": 1,
          "rating": 1,
          "shareHash": "string",
          "status": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
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
| `code` | number |  |
| `error` | boolean |  |
| `response.data.agencyId` | number |  |
| `response.data.blocked` | number |  |
| `response.data.companyId` | number |  |
| `response.data.createdAt` | date |  |
| `response.data.email` | string |  |
| `response.data.full` | string |  |
| `response.data.id` | number |  |
| `response.data.invited` | number |  |
| `response.data.job.active` | number |  |
| `response.data.job.agencyId` | number |  |
| `response.data.job.askCv` | number |  |
| `response.data.job.askMotivationLetter` | number |  |
| `response.data.job.blockTry` | number |  |
| `response.data.job.company.agencyId` | number |  |
| `response.data.job.company.createdAt` | date |  |
| `response.data.job.company.id` | number |  |
| `response.data.job.company.logo` | string |  |
| `response.data.job.company.name` | string |  |
| `response.data.job.company.permissions.createJobs` | boolean |  |
| `response.data.job.company.permissions.createRooms` | boolean |  |
| `response.data.job.company.permissions.editCompany` | boolean |  |
| `response.data.job.company.permissions.viewJobs` | boolean |  |
| `response.data.job.company.permissions.viewRooms` | boolean |  |
| `response.data.job.company.updatedAt` | date |  |
| `response.data.job.companyId` | number |  |
| `response.data.job.createdAt` | date |  |
| `response.data.job.description` | string |  |
| `response.data.job.forFollowUp` | number |  |
| `response.data.job.hashLink` | string |  |
| `response.data.job.id` | number |  |
| `response.data.job.interviewedCount` | number |  |
| `response.data.job.invitedCount` | number |  |
| `response.data.job.language` | string |  |
| `response.data.job.name` | string |  |
| `response.data.job.permissions.editJobs` | boolean |  |
| `response.data.job.permissions.rateResponses` | boolean |  |
| `response.data.job.previewVideo` | string |  |
| `response.data.job.randomOrder` | number |  |
| `response.data.job.startAt` | date |  |
| `response.data.job.updatedAt` | date |  |
| `response.data.jobId` | number |  |
| `response.data.language` | string |  |
| `response.data.overallCompatibility` | number |  |
| `response.data.permissions.rateResponses` | boolean |  |
| `response.data.pipelineIndex` | number |  |
| `response.data.rating` | number |  |
| `response.data.shareHash` | string |  |
| `response.data.status` | string |  |
| `response.data.updatedAt` | date |  |

## Native endpoint

Through the native HRBLADE API, this operation is `GET /response/get/:id` (base URL `https://api.hrblade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-response.md) for the provider-specific parameters and requirements.

