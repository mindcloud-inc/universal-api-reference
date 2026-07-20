# UserVitals Universal API Examples

These examples use the MindCloud API key and UserVitals connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Roadmap

Retrieves a roadmap by ID from the roadmap API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/get-roadmap?connectionId=$CONNECTION_ID&roadmapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roadmapId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/get-roadmap?${params}`, {
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

See the full [Get Roadmap action reference](actions/get-roadmap.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/userVitals/latest/actions/get-roadmap).

## Attach Feedback To Existing Item

Attaches feedback to an existing idea or story.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/attach-feedback-to-existing-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parentId": "string",
  "parentToken": "string",
  "sourceId": "string",
  "sourceToken": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/attach-feedback-to-existing-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parentId": "string",
    "parentToken": "string",
    "sourceId": "string",
    "sourceToken": "string"
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

See the full [Attach Feedback To Existing Item action reference](actions/attach-feedback-to-existing-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/userVitals/latest/actions/attach-feedback-to-existing-item).
