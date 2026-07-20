# Discourse Universal API Examples

These examples use the MindCloud API key and Discourse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Latest Topics

Retrieves the latest topics from Discourse.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-latest-topics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discourse/latest/actions/list-latest-topics?${params}`, {
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
      "flair_groups": [
        {}
      ],
      "primary_groups": [
        {}
      ],
      "topic_list": {},
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Latest Topics action reference](actions/list-latest-topics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/discourse/latest/actions/list-latest-topics).

## Activate User

Activates an existing user in Discourse.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discourse/latest/actions/activate-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discourse/latest/actions/activate-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
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
      "success": "string"
    }
  ],
  "meta": {}
}
```

See the full [Activate User action reference](actions/activate-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/discourse/latest/actions/activate-user).
