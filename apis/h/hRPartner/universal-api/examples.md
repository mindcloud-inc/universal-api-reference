# HR Partner Universal API Examples

These examples use the MindCloud API key and HR Partner connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-company?${params}`, {
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
      "activeEmployees": 1,
      "aiMonthlyApplicantLimit": 1,
      "employeeLimit": 1,
      "logoImageLink": "https://example.com",
      "name": "Ava Chen",
      "slug": "string",
      "smsCredits": 1,
      "subdomain": "string",
      "subscribed": true,
      "subscribedUntil": "2026-05-07T12:00:00.000Z",
      "timezone": "string",
      "totalEmployees": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Company action reference](actions/get-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hRPartner/latest/actions/get-company).

## Add or Update Applicant



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-applicant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-applicant', {
  method: 'PUT',
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
      "email": "ava@example.com",
      "firstNames": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "jobApplications": [
        {}
      ],
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

See the full [Add or Update Applicant action reference](actions/add-or-update-applicant.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hRPartner/latest/actions/add-or-update-applicant).
