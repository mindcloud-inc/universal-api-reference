# AssessTEAM Universal API Examples

These examples use the MindCloud API key and AssessTEAM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves the teams report from AssessTEAM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/list-teams?${params}`, {
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
      "averagescore": {},
      "description": {},
      "goalsetting": true,
      "location": {},
      "persons": 1,
      "teamname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assessTEAM/latest/actions/list-teams).

## Add Person

Creates a new person in AssessTEAM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/add-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "personCode": "string",
  "dateOfJoining": "string",
  "email": "ava@example.com",
  "contactNumber": "string",
  "team": "string",
  "jobTitle": "string",
  "enableSelfEvaluation": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assessTEAM/latest/actions/add-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "personCode": "string",
    "dateOfJoining": "string",
    "email": "ava@example.com",
    "contactNumber": "string",
    "team": "string",
    "jobTitle": "string",
    "enableSelfEvaluation": true
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
      "result": {
        "data": {},
        "message": "string",
        "personID": 1,
        "statusCode": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Person action reference](actions/add-person.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/assessTEAM/latest/actions/add-person).
