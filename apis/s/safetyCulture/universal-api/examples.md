# SafetyCulture Universal API Examples

These examples use the MindCloud API key and SafetyCulture connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Groups and Organizations

Retrieves groups and organizations from SafetyCulture.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/list-groups-and-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/list-groups-and-organizations?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Groups and Organizations action reference](actions/list-groups-and-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/safetyCulture/latest/actions/list-groups-and-organizations).

## Add Comment to Issue Timeline

Creates an issue timeline comment in SafetyCulture.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/add-comment-to-issue-timeline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/add-comment-to-issue-timeline', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "comment": "string"
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
      "value": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Comment to Issue Timeline action reference](actions/add-comment-to-issue-timeline.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/safetyCulture/latest/actions/add-comment-to-issue-timeline).
