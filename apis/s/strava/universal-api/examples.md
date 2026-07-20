# Strava Universal API Examples

These examples use the MindCloud API key and Strava connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated Athlete

Retrieves the authenticated athlete profile from Strava.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strava/latest/actions/get-authenticated-athlete?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strava/latest/actions/get-authenticated-athlete?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Authenticated Athlete action reference](actions/get-authenticated-athlete.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/strava/latest/actions/get-authenticated-athlete).

## Create Activity

Creates a new activity in Strava.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/strava/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "sportType": "string",
  "startDateLocal": "2026-05-07T12:00:00.000Z",
  "elapsedTime": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/strava/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "sportType": "string",
    "startDateLocal": "2026-05-07T12:00:00.000Z",
    "elapsedTime": 1
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

See the full [Create Activity action reference](actions/create-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/strava/latest/actions/create-activity).
