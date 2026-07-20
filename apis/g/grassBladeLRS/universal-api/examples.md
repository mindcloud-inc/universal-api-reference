# GrassBlade LRS Universal API Examples

These examples use the MindCloud API key and GrassBlade LRS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get About

Retrieves LRS about information from GrassBlade LRS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/get-about?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/get-about?${params}`, {
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

See the full [Get About action reference](actions/get-about.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/grassBladeLRS/latest/actions/get-about).

## Create Activity Profile

Stores or updates an activity profile in GrassBlade LRS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-activity-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "https://mindcloud.dev/grassblade/activity/stage3-20260406",
  "profileId": "mindcloud-activity-profile-stage3",
  "document": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grassBladeLRS/latest/actions/create-activity-profile', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "https://mindcloud.dev/grassblade/activity/stage3-20260406",
    "profileId": "mindcloud-activity-profile-stage3",
    "document": "[object Object]"
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

See the full [Create Activity Profile action reference](actions/create-activity-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/grassBladeLRS/latest/actions/create-activity-profile).
