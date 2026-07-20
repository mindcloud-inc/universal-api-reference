# ForceManager Universal API Examples

These examples use the MindCloud API key and ForceManager connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Read Activities

Retrieves activities from your ForceManager account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-activities?${params}`, {
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
      "accountId": 1,
      "activityDateTime": "2026-05-07T12:00:00.000Z",
      "comment": "string",
      "contactId": 1,
      "id": 1,
      "isCheckin": true,
      "salesRepId": 1
    }
  ],
  "meta": {}
}
```

See the full [Read Activities action reference](actions/read-activities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/forceManager/latest/actions/read-activities).

## Create Activity

Creates a new activity in ForceManager.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityDateTime": "2026-05-07T12:00:00.000Z",
  "salesRepId": 1,
  "accountId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityDateTime": "2026-05-07T12:00:00.000Z",
    "salesRepId": 1,
    "accountId": 1
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
      "accountId": 1,
      "activityDateTime": "2026-05-07T12:00:00.000Z",
      "comment": "string",
      "contactId": 1,
      "id": 1,
      "isCheckin": true,
      "salesRepId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Activity action reference](actions/create-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/forceManager/latest/actions/create-activity).
