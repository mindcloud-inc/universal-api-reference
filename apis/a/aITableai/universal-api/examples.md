# AITable.ai Universal API Examples

These examples use the MindCloud API key and AITable.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Member

Retrieves a member from a space in AITable.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/get-member?connectionId=$CONNECTION_ID&spaceId=string&unitId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string",
  "unitId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/get-member?${params}`, {
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
      "avatar": "string",
      "name": "Ava Chen",
      "unitId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Member action reference](actions/get-member.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aITableai/latest/actions/get-member).

## Create Datasheet

Creates a new datasheet in AITable.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-datasheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/create-datasheet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "name": "Ava Chen"
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
      "createdAt": 1,
      "fields": [
        {}
      ],
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Datasheet action reference](actions/create-datasheet.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aITableai/latest/actions/create-datasheet).
