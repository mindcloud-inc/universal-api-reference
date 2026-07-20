# Reteach Universal API Examples

These examples use the MindCloud API key and Reteach connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Customer



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerIdentifier=2bf64377-4a26-4439-9c69-323b9111ea70" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerIdentifier": "2bf64377-4a26-4439-9c69-323b9111ea70"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reteach/latest/actions/get-customer?${params}`, {
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
      "authenticationMethod": "string",
      "birthDate": "string",
      "company": "string",
      "department": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "expiredNotificationMail": "string",
      "externalId": "string",
      "firstName": "Ava",
      "gender": "string",
      "id": "string",
      "language": "string",
      "lastLoginAt": "string",
      "lastName": "Chen",
      "location": "string",
      "manager": {},
      "managerId": "string",
      "note": "string",
      "position": "string",
      "registeredAt": "string",
      "setActiveAt": "string",
      "setInactiveAt": "string",
      "source": "string",
      "status": "string",
      "tags": [
        {}
      ],
      "team": "string",
      "timezone": "string",
      "userName": "Ava Chen",
      "userType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Customer action reference](actions/get-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reteach/latest/actions/get-customer).
