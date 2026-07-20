# actiTIME Universal API Examples

These examples use the MindCloud API key and actiTIME connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves a list of users from actiTIME.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-users?${params}`, {
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
      "allowedActions": {
        "canSubmitTimetrack": true
      },
      "departmentId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "hired": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastName": "Chen",
      "middleName": "Ava Chen",
      "releaseDate": "2026-05-07T12:00:00.000Z",
      "timeZoneGroupId": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/actiTIME/latest/actions/list-users).
