# HoorayHR Universal API Examples

These examples use the MindCloud API key and HoorayHR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves employee records from the HoorayHR directory.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hoorayHR/latest/actions/list-users?${params}`, {
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
      "civilStatus": "string",
      "companyId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "entityId": 1,
      "firstName": "Ava",
      "gender": "string",
      "holidayPolicyId": 1,
      "id": 1,
      "isAdmin": 1,
      "isDemoData": true,
      "lastName": "Chen",
      "lastNameUsage": "Chen",
      "locale": "string",
      "nationality": "string",
      "status": 1,
      "timezone": "string",
      "travelAllowance": 1,
      "travelAllowanceCurrency": "string",
      "twoFactorAuthentication": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hoorayHR/latest/actions/list-users).
