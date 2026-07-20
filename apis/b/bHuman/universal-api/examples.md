# BHuman Universal API Examples

These examples use the MindCloud API key and BHuman connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces

Retrieves available account workspaces from BHuman.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/list-workspaces?${params}`, {
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
      "code": 1,
      "result": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": 1,
          "name": "Ava Chen",
          "role": "string",
          "token": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "userId": "string",
          "workspaceId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bHuman/latest/actions/list-workspaces).

## Generate Video by Campaign

Creates personalized videos from a campaign in BHuman.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/generate-video-by-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "namesJson": "Ava Chen",
  "variablesJson": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/generate-video-by-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "namesJson": "Ava Chen",
    "variablesJson": "string"
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

See the full [Generate Video by Campaign action reference](actions/generate-video-by-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bHuman/latest/actions/generate-video-by-campaign).
