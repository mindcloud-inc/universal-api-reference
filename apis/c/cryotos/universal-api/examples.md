# Cryotos Universal API Examples

These examples use the MindCloud API key and Cryotos connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryotos/latest/actions/get-current-user?${params}`, {
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
      "activated": true,
      "authorities": [
        "string"
      ],
      "communicationEmail": "ava@example.com",
      "companyId": 1,
      "countryCode": "string",
      "dateFormat": "string",
      "dateTimeFormat": "string",
      "designation": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "langKey": "string",
      "lastName": "Chen",
      "mobilePhone": "string",
      "passwordExpired": true,
      "roleName": "Ava Chen",
      "tenantId": "string",
      "userGroupIds": [
        1
      ],
      "userGroupNames": [
        "Ava Chen"
      ],
      "workflowType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cryotos/latest/actions/get-current-user).
