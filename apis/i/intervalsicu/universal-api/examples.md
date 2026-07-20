# Intervals.icu Universal API Examples

These examples use the MindCloud API key and Intervals.icu connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Athlete

Retrieves an athlete from Intervals.icu.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/get-athlete?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/get-athlete?${params}`, {
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

See the full [Get Athlete action reference](actions/get-athlete.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intervalsicu/latest/actions/get-athlete).

## Add Activity Message

Adds an activity message in Intervals.icu.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/add-activity-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/add-activity-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Add Activity Message action reference](actions/add-activity-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/intervalsicu/latest/actions/add-activity-message).
