# Motive Universal API Examples

These examples use the MindCloud API key and Motive connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List users



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/motive/latest/actions/list-users?${params}`, {
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
      "user": {
        "companyReferenceId": {},
        "createdAt": "string",
        "email": "ava@example.com",
        "expiresAt": {},
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen",
        "metricUnits": true,
        "mobileCurrentSignInAt": {},
        "mobileLastActiveAt": {},
        "mobileLastSignInAt": {},
        "phone": "string",
        "phone2": {},
        "phoneCountryCode": "string",
        "phoneCountryCode2": {},
        "phoneExt": "string",
        "role": "string",
        "status": "string",
        "timeZone": "string",
        "updatedAt": "string",
        "webCurrentSignInAt": "string",
        "webLastActiveAt": "string",
        "webLastSignInAt": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [List users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/motive/latest/actions/list-users).
