# Teachlr Organizations Universal API Examples

These examples use the MindCloud API key and Teachlr Organizations connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User by Email



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-user-by-email?connectionId=$CONNECTION_ID&email=apps%40mindcloud.co" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "apps@mindcloud.co"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-user-by-email?${params}`, {
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
      "about": {},
      "agreeTerms": true,
      "agreeTermsAt": {},
      "alternativeId": {},
      "city": {},
      "country": {},
      "countryIsoCode": {},
      "createdAt": "string",
      "department": {},
      "email": "ava@example.com",
      "employeeNumber": "string",
      "externalId": "string",
      "firstLoginAt": {},
      "id": 1,
      "identificationNumber": {},
      "job": {},
      "language": "string",
      "lastActivityAt": {},
      "lastLoginAt": {},
      "lastName": "Chen",
      "name": "Ava Chen",
      "numVisit": 1,
      "organizationId": 1,
      "organizationName": {},
      "phone": {},
      "picture": {
        "large": "string",
        "medium": "string",
        "small": "string",
        "thumb": "string"
      },
      "registerType": "string",
      "subscriber": true,
      "tempEmail": true,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get User by Email action reference](actions/get-user-by-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teachlrOrganizations/latest/actions/get-user-by-email).

## Create Meeting



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/create-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "apps@mindcloud.co",
  "topic": "MindCloud Test Meeting",
  "date": "2026-04-03",
  "time": "10:00",
  "duration": "30",
  "timezone": "America/Sao_Paulo"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/create-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "apps@mindcloud.co",
    "topic": "MindCloud Test Meeting",
    "date": "2026-04-03",
    "time": "10:00",
    "duration": "30",
    "timezone": "America/Sao_Paulo"
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
      "date": "string",
      "duration": 1,
      "hostEmail": "ava@example.com",
      "meetingId": 1,
      "time": "string",
      "timezone": "string",
      "topic": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Meeting action reference](actions/create-meeting.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teachlrOrganizations/latest/actions/create-meeting).
