# TalentHR: Get Directory

Retrieves the employee directory from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-directory?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/get-directory?${params}`, {
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
| `limit` | number | no | Maximum number of employees to return. TalentHR defaults to 10 when this is omitted. |
| `offset` | number | no | Pagination offset. Use -1 to disable pagination for this endpoint. |
| `filter` | string | no | Optional directory filter ID. Use the Directory Filters endpoint to discover valid filter IDs before using this field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeCycle": 1,
      "department": "string",
      "departmentId": 1,
      "division": "string",
      "divisionId": 1,
      "email": "ava@example.com",
      "employmentStatusId": 1,
      "employmentStatusName": "Ava Chen",
      "firstName": "Ava",
      "hireDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isFutureRehire": true,
      "isOwner": 1,
      "jobTitle": "string",
      "jobTitleId": 1,
      "lastName": "Chen",
      "linkedInUrl": "https://example.com",
      "location": "string",
      "locationId": 1,
      "photoUrl": "https://example.com",
      "reportsToEmployeeId": 1,
      "resizedPhotoUrl": "https://example.com",
      "terminationDate": "2026-05-07T12:00:00.000Z",
      "timeOffRequests": [
        {}
      ],
      "userId": 1,
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
| `activeCycle` | number | Current active cycle identifier. |
| `department` | string | Department name. |
| `departmentId` | number | Department ID. |
| `division` | string | Division name. |
| `divisionId` | number | Division ID. |
| `email` | string | Employee email address. |
| `employmentStatusId` | number | Employment status ID. |
| `employmentStatusName` | string | Employment status name. |
| `firstName` | string | Employee first name. |
| `hireDate` | date | Employee hire date. |
| `id` | number | TalentHR employee record ID. |
| `isFutureRehire` | boolean | Whether the employee is marked as a future rehire. |
| `isOwner` | number | Whether the employee is the workspace owner. |
| `jobTitle` | string | Job title name. |
| `jobTitleId` | number | Job title ID. |
| `lastName` | string | Employee last name. |
| `linkedInUrl` | string | LinkedIn profile URL when present. |
| `location` | string | Location name. |
| `locationId` | number | Location ID. |
| `photoUrl` | string | Original employee photo URL. |
| `reportsToEmployeeId` | number | Manager employee ID when available. |
| `resizedPhotoUrl` | string | Resized employee photo URL. |
| `terminationDate` | date | Employee termination date when present. |
| `timeOffRequests` | array<object> | Time off requests linked to the employee. |
| `userId` | number | Related user ID. |
| `userRole` | object | Nested user role details for the employee. |
| `workPhone` | string | Work phone number. |

## Native endpoint

Through the native TalentHR API, this operation is `GET /directory` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-directory.md) for the provider-specific parameters and requirements.

