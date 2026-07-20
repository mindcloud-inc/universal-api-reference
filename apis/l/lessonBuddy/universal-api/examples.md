# LessonBuddy Universal API Examples

These examples use the MindCloud API key and LessonBuddy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Published Locations

Retrieves published locations from LessonBuddy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/list-published-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/list-published-locations?${params}`, {
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
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "hours": [
        {}
      ],
      "id": 1,
      "mapUrl": "https://example.com",
      "name": "Ava Chen",
      "openDate": "2026-05-07T12:00:00.000Z",
      "phoneNumber": "string",
      "regionSlug": "string",
      "slug": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Published Locations action reference](actions/list-published-locations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lessonBuddy/latest/actions/list-published-locations).

## Create Lead

Creates a new lead in LessonBuddy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "locationId": 1,
  "firstName": "Ava",
  "lastName": "Chen",
  "emailAddress": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "locationId": 1,
    "firstName": "Ava",
    "lastName": "Chen",
    "emailAddress": "ava@example.com"
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
      "campaignId": 1,
      "clientPlatformId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdById": 1,
      "familyId": 1,
      "id": 1,
      "locationId": 1,
      "meta": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedById": 1,
      "utmCodeId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Lead action reference](actions/create-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lessonBuddy/latest/actions/create-lead).
