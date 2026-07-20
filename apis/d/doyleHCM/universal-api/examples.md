# Doyle HCM Universal API Examples

These examples use the MindCloud API key and Doyle HCM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get current user

Retrieves the current user profile from Doyle HCM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/get-current-user?${params}`, {
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
      "allClientsAccess": true,
      "companies": [
        {}
      ],
      "login": {},
      "partnerId": 1,
      "role": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get current user action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/doyleHCM/latest/actions/get-current-user).

## Create company department

Creates a company department in Doyle HCM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/create-company-department" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/doyleHCM/latest/actions/create-company-department', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
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
      "id": 1,
      "name": "Ava Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create company department action reference](actions/create-company-department.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/doyleHCM/latest/actions/create-company-department).
