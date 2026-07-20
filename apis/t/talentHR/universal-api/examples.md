# TalentHR Universal API Examples

These examples use the MindCloud API key and TalentHR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Directory

Retrieves the employee directory from TalentHR.

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

Example response:

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

See the full [Get Directory action reference](actions/get-directory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/talentHR/latest/actions/get-directory).

## Create Benefit Category

Creates a new benefit category in TalentHR.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-benefit-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/create-benefit-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "deletedAt": "string",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Benefit Category action reference](actions/create-benefit-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/talentHR/latest/actions/create-benefit-category).
