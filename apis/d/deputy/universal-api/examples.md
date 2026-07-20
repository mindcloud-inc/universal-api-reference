# Deputy Universal API Examples

These examples use the MindCloud API key and Deputy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Employees

Retrieves the employee list from Deputy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deputy/latest/actions/list-employees?${params}`, {
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
      "active": true,
      "allowAppraisal": true,
      "company": 1,
      "contact": 1,
      "created": "string",
      "creator": 1,
      "customFieldData": {},
      "customPronouns": {},
      "dateOfBirth": {},
      "displayName": "Ava Chen",
      "DPMetaData": {
        "creatorInfo": {
          "customPronouns": {},
          "displayName": "Ava Chen",
          "employee": 1,
          "employeeProfile": 1,
          "id": 1,
          "photo": "string",
          "pronouns": 1
        },
        "system": "string"
      },
      "emergencyAddress": {},
      "employmentEndComment": {},
      "employmentEndDate": {},
      "employmentEndReason": {},
      "employmentEndSentiment": {},
      "externalLinkId": {},
      "firstName": "Ava",
      "gender": {},
      "higherDuty": {},
      "historyId": 1,
      "id": 1,
      "jobAppId": {},
      "lastName": "Chen",
      "mainAddress": {},
      "modified": "string",
      "onboardingId": {},
      "otherName": {},
      "photo": {},
      "position": "string",
      "postalAddress": {},
      "pronouns": 1,
      "role": 1,
      "salutation": {},
      "startDate": "string",
      "stressProfile": 1,
      "terminationDate": {},
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [List Employees action reference](actions/list-employees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deputy/latest/actions/list-employees).

## Add Shift

Creates a new shift in Deputy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deputy/latest/actions/add-shift" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deputy/latest/actions/add-shift', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "_DPMetaData": {},
      "Comment": "string",
      "ConfirmStatus": 1,
      "Created": "2026-05-07T12:00:00.000Z",
      "Date": "2026-05-07T12:00:00.000Z",
      "Employee": 1,
      "EndTime": 1,
      "EndTimeLocalized": "2026-05-07T12:00:00.000Z",
      "Id": 1,
      "Mealbreak": "2026-05-07T12:00:00.000Z",
      "Modified": "2026-05-07T12:00:00.000Z",
      "OperationalUnit": 1,
      "Published": true,
      "Slots": [
        {}
      ],
      "StartTime": 1,
      "StartTimeLocalized": "2026-05-07T12:00:00.000Z",
      "TotalTime": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Shift action reference](actions/add-shift.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deputy/latest/actions/add-shift).
