# UseINBOX Universal API Examples

These examples use the MindCloud API key and UseINBOX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Campaigns

Retrieves campaigns from UseINBOX.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-all-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-all-campaigns?${params}`, {
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
      "createTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "plannedTime": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "subject": "string",
      "updateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get All Campaigns action reference](actions/get-all-campaigns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/useINBOX/latest/actions/get-all-campaigns).

## Add Single Contact To List

Adds a contact to a list in UseINBOX.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/add-single-contact-to-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/add-single-contact-to-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "email": "ava@example.com"
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
      "email": "ava@example.com",
      "id": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Single Contact To List action reference](actions/add-single-contact-to-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/useINBOX/latest/actions/add-single-contact-to-list).
