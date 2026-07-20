# Quilia Universal API Examples

These examples use the MindCloud API key and Quilia connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current API Key Information



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/get-current-api-key-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quilia/latest/actions/get-current-api-key-information?${params}`, {
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

See the full [Get Current API Key Information action reference](actions/get-current-api-key-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quilia/latest/actions/get-current-api-key-information).

## Create Appointment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "caseId": "string",
  "start": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quilia/latest/actions/create-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "caseId": "string",
    "start": "2026-05-07T12:00:00.000Z"
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

See the full [Create Appointment action reference](actions/create-appointment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quilia/latest/actions/create-appointment).
