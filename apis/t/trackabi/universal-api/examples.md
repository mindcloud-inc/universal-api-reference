# Trackabi Universal API Examples

These examples use the MindCloud API key and Trackabi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Details

Retrieves company details from Trackabi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-company-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/get-company-details?${params}`, {
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
      "address": "string",
      "alias": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company Details action reference](actions/get-company-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trackabi/latest/actions/get-company-details).

## Assign Project Members

Assigns members to a project in Trackabi.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/assign-project-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "[]": [
    {}
  ],
  "[].memberId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/assign-project-members', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "[]": [{}],
    "[].memberId": 1
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
      "assignedMembers": [
        {
          "address": "string",
          "avatar": "string",
          "birthdate": "string",
          "education": "string",
          "email": "ava@example.com",
          "emergencyContact": "string",
          "emergencyPhone": "string",
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "notes": "string",
          "personalEmail": "ava@example.com",
          "phone": "string"
        }
      ],
      "client": {
        "address": "string",
        "contactPerson": "string",
        "costHourlyRate": 1,
        "currency": "string",
        "email": "ava@example.com",
        "hourlyRate": 1,
        "id": 1,
        "logo": "string",
        "name": "Ava Chen",
        "notes": "string",
        "phone": "string",
        "shortName": "Ava Chen"
      },
      "costHourlyRate": "https://example.com",
      "currency": "string",
      "description": "string",
      "endDate": "string",
      "estimateUnits": "string",
      "hourlyRate": 1,
      "id": 1,
      "name": "Ava Chen",
      "notBillable": 1,
      "shortName": "Ava Chen",
      "startDate": "string",
      "teams": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Assign Project Members action reference](actions/assign-project-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trackabi/latest/actions/assign-project-members).
