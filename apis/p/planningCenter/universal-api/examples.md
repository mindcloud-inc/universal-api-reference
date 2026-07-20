# Planning Center Universal API Examples

These examples use the MindCloud API key and Planning Center connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List People

Retrieves people from Planning Center.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/list-people?${params}`, {
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
      "attributes": {
        "accountingAdministrator": true,
        "anniversary": "2026-05-07T12:00:00.000Z",
        "avatar": "string",
        "birthdate": "2026-05-07T12:00:00.000Z",
        "canCreateForms": true,
        "canEmailLists": true,
        "child": true,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "demographicAvatarUrl": "https://example.com",
        "directoryStatus": "string",
        "firstName": "Ava",
        "gender": "string",
        "givenName": "Ava Chen",
        "grade": 1,
        "graduationYear": 1,
        "inactivatedAt": "2026-05-07T12:00:00.000Z",
        "lastName": "Chen",
        "loginIdentifier": "string",
        "medicalNotes": "string",
        "membership": "string",
        "mfaConfigured": true,
        "middleName": "Ava Chen",
        "name": "Ava Chen",
        "nickname": "Ava Chen",
        "passedBackgroundCheck": true,
        "peoplePermissions": "string",
        "remoteId": 1,
        "resourcePermissionFlags": {
          "canAccessWorkflows": true
        },
        "schoolType": "string",
        "siteAdministrator": true,
        "status": "string",
        "stripeCustomerIdentifier": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List People action reference](actions/list-people.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/planningCenter/latest/actions/list-people).

## Create Household

Creates a new household in Planning Center.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/create-household" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planningCenter/latest/actions/create-household', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {}
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
      "attributes": {
        "avatar": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "memberCount": 1,
        "name": "Ava Chen",
        "primaryContactId": "string",
        "primaryContactName": "Ava Chen",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "id": "string",
      "relationships": {
        "people": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        },
        "primaryContact": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Household action reference](actions/create-household.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/planningCenter/latest/actions/create-household).
