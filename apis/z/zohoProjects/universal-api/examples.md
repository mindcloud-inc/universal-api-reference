# Zoho Projects Universal API Examples

These examples use the MindCloud API key and Zoho Projects connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Portals

Retrieves portals from Zoho Projects.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-portals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/list-portals?${params}`, {
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
      "bugPlan": "string",
      "id": "string",
      "isDefaultPortal": true,
      "orgLogo": "string",
      "orgName": "Ava Chen",
      "owner": {
        "businessHoursId": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "id": "string",
        "isClientUser": true,
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string"
      },
      "portalName": "Ava Chen",
      "portalOwner": "string",
      "portalType": "string",
      "portalUrl": "https://example.com",
      "profile": {
        "id": "string",
        "name": "Ava Chen"
      },
      "profileId": "string",
      "projectPlan": "string",
      "timezone": "string",
      "zsoid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Portals action reference](actions/list-portals.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoProjects/latest/actions/list-portals).

## Create Issue

Creates a new issue in Zoho Projects.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": "string",
  "projectId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": "string",
    "projectId": "string",
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
      "addedVia": "string",
      "assignee": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      },
      "classification": {
        "id": "string",
        "value": "string"
      },
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "flag": "string",
      "id": "string",
      "isItReproducible": {
        "id": "string",
        "value": "string"
      },
      "lastUpdatedTime": "2026-05-07T12:00:00.000Z",
      "module": {
        "id": "string",
        "value": "string"
      },
      "name": "Ava Chen",
      "prefix": "string",
      "project": {
        "id": "string",
        "name": "Ava Chen"
      },
      "severity": {
        "id": "string",
        "value": "string"
      },
      "status": {
        "color": "string",
        "colorHexcode": "string",
        "id": "string",
        "isClosedType": true,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Issue action reference](actions/create-issue.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoProjects/latest/actions/create-issue).
