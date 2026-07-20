# SignWell Universal API Examples

These examples use the MindCloud API key and SignWell connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credentials

Retrieves account and user details from SignWell.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signWell/latest/actions/get-credentials?${params}`, {
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
      "account": {
        "activeTemplates": 1,
        "activeUsers": [
          {
            "email": "ava@example.com",
            "hasGoogleRegistration": true,
            "id": "string",
            "name": "Ava Chen"
          }
        ],
        "canCreateCompletionDocument": true,
        "canCreateTemplate": true,
        "canCreateTrackingDocument": true,
        "id": "string",
        "name": "Ava Chen",
        "planTier": "string"
      },
      "archived": true,
      "contact": {
        "altPhoneNumber": {},
        "archived": true,
        "companyName": {},
        "email": "ava@example.com",
        "id": "string",
        "initials": "string",
        "name": "Ava Chen",
        "phoneNumber": {},
        "website": {}
      },
      "id": "string",
      "role": "string",
      "user": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "hasGoogleRegistration": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "workspace": {
        "activeTemplates": 1,
        "activeUsers": [
          {
            "email": "ava@example.com",
            "hasGoogleRegistration": true,
            "id": "string",
            "name": "Ava Chen"
          }
        ],
        "canCreateCompletionDocument": true,
        "canCreateTemplate": true,
        "canCreateTrackingDocument": true,
        "id": "string",
        "name": "Ava Chen",
        "planTier": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Credentials action reference](actions/get-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signWell/latest/actions/get-credentials).

## Create Bulk Send

Creates a new bulk send in SignWell.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-bulk-send" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateIds[]": [
    "string"
  ],
  "bulkSendCsv": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signWell/latest/actions/create-bulk-send', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateIds[]": ["string"],
    "bulkSendCsv": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Bulk Send action reference](actions/create-bulk-send.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/signWell/latest/actions/create-bulk-send).
