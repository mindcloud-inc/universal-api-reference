# Verix Universal API Examples

These examples use the MindCloud API key and Verix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Groups

Retrieves credential groups from your Verix account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verix/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verix/latest/actions/list-groups?${params}`, {
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
      "createTime": 1,
      "description": "string",
      "id": 1,
      "issuedRecipient": 1,
      "name": "Ava Chen",
      "templateImageRelUrl": "https://example.com",
      "totalRecipient": 1
    }
  ],
  "meta": {}
}
```

See the full [List Groups action reference](actions/list-groups.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verix/latest/actions/list-groups).

## Create Multiple Credentials

Creates multiple credentials in Verix for a group.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verix/latest/actions/create-multiple-credentials" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_id": "894",
  "inputs[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verix/latest/actions/create-multiple-credentials', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_id": "894",
    "inputs[]": "[object Object]"
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
      "requestId": 1,
      "responseQueue": [
        {
          "credentialUid": "string",
          "recipientExternalId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Multiple Credentials action reference](actions/create-multiple-credentials.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/verix/latest/actions/create-multiple-credentials).
