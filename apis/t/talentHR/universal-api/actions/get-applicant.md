# TalentHR: Get Applicant

Retrieves an applicant from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-applicant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-applicant?connectionId=$CONNECTION_ID&objectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-applicant?${params}`, {
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
| `objectId` | number | yes | TalentHR applicant ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedAt": "2026-05-07T12:00:00.000Z",
      "address": "string",
      "applications": [
        {}
      ],
      "applicationsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "latestApplicationId": 1,
      "latestCv": {},
      "latestCvId": 1,
      "phone": "string",
      "starred": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedAt` | date |  |
| `address` | string |  |
| `applications` | array<object> |  |
| `applicationsCount` | number |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `description` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `latestApplicationId` | number |  |
| `latestCv` | object |  |
| `latestCvId` | number |  |
| `phone` | string |  |
| `starred` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /ats-applicants/:objectId` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-applicant.md) for the provider-specific parameters and requirements.

