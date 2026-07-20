# TalentHR: Get Employee

Retrieves an employee from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-employee?connectionId=$CONNECTION_ID&employee=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employee": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-employee?${params}`, {
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
| `employee` | number | yes | TalentHR employee ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeCycle": 1,
      "address": "string",
      "birthDate": "2026-05-07T12:00:00.000Z",
      "citizenship": "string",
      "city": "string",
      "country": "string",
      "customFields": [
        {}
      ],
      "defaultAvatar": true,
      "departmentId": 1,
      "departmentName": "Ava Chen",
      "divisionId": 1,
      "divisionName": "Ava Chen",
      "emergencyContact": {},
      "employeeNumber": "string",
      "gender": "string",
      "hireDate": "2026-05-07T12:00:00.000Z",
      "hireDateUtc": "string",
      "hirePacket": {},
      "id": 1,
      "isFutureRehire": true,
      "isTerminated": true,
      "jobTitleId": 1,
      "jobTitleName": "Ava Chen",
      "linkedInUrl": "https://example.com",
      "locationId": 1,
      "locationName": "Ava Chen",
      "maritalStatus": "string",
      "nationality": "string",
      "personalEmail": "ava@example.com",
      "photoUrl": "https://example.com",
      "postalCode": "string",
      "resizedPhotoUrl": "https://example.com",
      "seniority": {},
      "shortManager": {},
      "terminationDate": "2026-05-07T12:00:00.000Z",
      "terminationReason": "string",
      "user": {},
      "userRole": {},
      "workPhone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeCycle` | number |  |
| `address` | string |  |
| `birthDate` | date |  |
| `citizenship` | string |  |
| `city` | string |  |
| `country` | string |  |
| `customFields` | array<object> |  |
| `defaultAvatar` | boolean |  |
| `departmentId` | number |  |
| `departmentName` | string |  |
| `divisionId` | number |  |
| `divisionName` | string |  |
| `emergencyContact` | object |  |
| `employeeNumber` | string |  |
| `gender` | string |  |
| `hireDate` | date |  |
| `hireDateUtc` | string |  |
| `hirePacket` | object |  |
| `id` | number |  |
| `isFutureRehire` | boolean |  |
| `isTerminated` | boolean |  |
| `jobTitleId` | number |  |
| `jobTitleName` | string |  |
| `linkedInUrl` | string |  |
| `locationId` | number |  |
| `locationName` | string |  |
| `maritalStatus` | string |  |
| `nationality` | string |  |
| `personalEmail` | string |  |
| `photoUrl` | string |  |
| `postalCode` | string |  |
| `resizedPhotoUrl` | string |  |
| `seniority` | object |  |
| `shortManager` | object |  |
| `terminationDate` | date |  |
| `terminationReason` | string |  |
| `user` | object |  |
| `userRole` | object |  |
| `workPhone` | string |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /employees/:employee` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

