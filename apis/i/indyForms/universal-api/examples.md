# IndyForms Universal API Examples

These examples use the MindCloud API key and IndyForms connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/list-forms?${params}`, {
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
      "completedRecordCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "folder": "string",
      "id": "string",
      "isLive": true,
      "name": "Ava Chen",
      "recordCount": 1,
      "tags": [
        "string"
      ],
      "version": 1,
      "versionId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/indyForms/latest/actions/list-forms).

## Create Webhook



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/indyForms/latest/actions/create-webhook', {
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
  "data": [
    {
      "description": "string",
      "endpointAddress": "string",
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "raisedFor": [
        "string"
      ],
      "sharedSecret": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/indyForms/latest/actions/create-webhook).
