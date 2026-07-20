# HRBLADE: Get Job



```
GET https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HRBLADE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-job?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRBLADE/latest/actions/get-job?${params}`, {
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
| `id` | number | yes | Job identifier. |

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
          "active": 1,
          "agency": {
            "aiRequestsCount": 1,
            "aiRequestsLimit": 1,
            "clientType": "string",
            "companiesLimit": 1,
            "countryCode": "string",
            "createdAt": "2026-05-07T12:00:00.000Z",
            "id": 1,
            "interviewsLimit": 1,
            "planId": 1,
            "quantity": 1,
            "responsesLimit": 1,
            "updatedAt": "2026-05-07T12:00:00.000Z",
            "usersLimit": 1,
            "videoDefinition": "string"
          },
          "agencyId": 1,
          "askCv": 1,
          "askMotivationLetter": 1,
          "blockTry": 1,
          "canExportAll": true,
          "company": {
            "id": 1,
            "name": "Ava Chen",
            "permissions": {
              "createJobs": true,
              "createRooms": true,
              "editCompany": true,
              "viewJobs": true,
              "viewRooms": true
            }
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
| `response.data.active` | number |  |
| `response.data.agency.aiRequestsCount` | number |  |
| `response.data.agency.aiRequestsLimit` | number |  |
| `response.data.agency.clientType` | string |  |
| `response.data.agency.companiesLimit` | number |  |
| `response.data.agency.countryCode` | string |  |
| `response.data.agency.createdAt` | date |  |
| `response.data.agency.id` | number |  |
| `response.data.agency.interviewsLimit` | number |  |
| `response.data.agency.planId` | number |  |
| `response.data.agency.quantity` | number |  |
| `response.data.agency.responsesLimit` | number |  |
| `response.data.agency.updatedAt` | date |  |
| `response.data.agency.usersLimit` | number |  |
| `response.data.agency.videoDefinition` | string |  |
| `response.data.agencyId` | number |  |
| `response.data.askCv` | number |  |
| `response.data.askMotivationLetter` | number |  |
| `response.data.blockTry` | number |  |
| `response.data.canExportAll` | boolean |  |
| `response.data.company.id` | number |  |
| `response.data.company.name` | string |  |
| `response.data.company.permissions.createJobs` | boolean |  |
| `response.data.company.permissions.createRooms` | boolean |  |
| `response.data.company.permissions.editCompany` | boolean |  |
| `response.data.company.permissions.viewJobs` | boolean |  |
| `response.data.company.permissions.viewRooms` | boolean |  |
| `response.data.companyId` | number |  |
| `response.data.createdAt` | date |  |
| `response.data.description` | string |  |
| `response.data.forFollowUp` | number |  |
| `response.data.hashLink` | string |  |
| `response.data.id` | number |  |
| `response.data.interviewedCount` | number |  |
| `response.data.invitedCount` | number |  |
| `response.data.language` | string |  |
| `response.data.name` | string |  |
| `response.data.permissions.editJobs` | boolean |  |
| `response.data.permissions.rateResponses` | boolean |  |
| `response.data.previewVideo` | string |  |
| `response.data.randomOrder` | number |  |
| `response.data.startAt` | date |  |
| `response.data.updatedAt` | date |  |

## Native endpoint

Through the native HRBLADE API, this operation is `GET /job/get/:id` (base URL `https://api.hrblade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

