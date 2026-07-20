# EasyContent Universal API Examples

These examples use the MindCloud API key and EasyContent connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check API Key

Checks an EasyContent API key and returns its project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/check-api-key?${params}`, {
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
      "projectId": 1,
      "projectTitle": "string",
      "projectUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Check API Key action reference](actions/check-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyContent/latest/actions/check-api-key).

## Change Content Item Assignees And Due Dates

Updates assignees or due dates for an EasyContent item.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/change-content-item-assignees-and-due-dates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "articleId": 1,
  "statusId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyContent/latest/actions/change-content-item-assignees-and-due-dates', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "articleId": 1,
    "statusId": 1
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

See the full [Change Content Item Assignees And Due Dates action reference](actions/change-content-item-assignees-and-due-dates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyContent/latest/actions/change-content-item-assignees-and-due-dates).
