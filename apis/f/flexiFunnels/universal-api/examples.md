# FlexiFunnels Universal API Examples

These examples use the MindCloud API key and FlexiFunnels connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Profile

Retrieves the authenticated member profile from FlexiFunnels.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/get-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/get-profile?${params}`, {
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

See the full [Get Profile action reference](actions/get-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flexiFunnels/latest/actions/get-profile).

## Mark Complete

Marks a lesson complete in FlexiFunnels.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/mark-complete" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "funnelPageId": "1027516",
  "courseId": "91090",
  "lessonId": "545366"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexiFunnels/latest/actions/mark-complete', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "funnelPageId": "1027516",
    "courseId": "91090",
    "lessonId": "545366"
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

See the full [Mark Complete action reference](actions/mark-complete.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flexiFunnels/latest/actions/mark-complete).
