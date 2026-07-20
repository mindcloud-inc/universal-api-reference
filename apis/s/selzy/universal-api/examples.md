# Selzy Universal API Examples

These examples use the MindCloud API key and Selzy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contact Lists

Retrieves contact lists from Selzy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-contact-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/selzy/latest/actions/list-contact-lists?${params}`, {
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
      "result": [
        {
          "id": 1,
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Contact Lists action reference](actions/list-contact-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/selzy/latest/actions/list-contact-lists).

## Cancel Campaign

Cancels a scheduled campaign in Selzy.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/selzy/latest/actions/cancel-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/selzy/latest/actions/cancel-campaign', {
  method: 'PUT',
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
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Cancel Campaign action reference](actions/cancel-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/selzy/latest/actions/cancel-campaign).
