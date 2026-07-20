# Sequenzy Universal API Examples

These examples use the MindCloud API key and Sequenzy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Metrics

Retrieves account engagement metrics from Sequenzy.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-account-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/get-account-metrics?${params}`, {
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
      "period": "string",
      "stats": {
        "clicked": 1,
        "clickRate": 1,
        "delivered": 1,
        "deliveryRate": 1,
        "opened": 1,
        "openRate": 1,
        "sent": 1,
        "unsubscribed": 1,
        "unsubscribeRate": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Get Account Metrics action reference](actions/get-account-metrics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sequenzy/latest/actions/get-account-metrics).

## Add Tag

Adds a tag to a subscriber in Sequenzy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/add-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sequenzy/latest/actions/add-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "tag": "string"
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
      "subscriber": {
        "created": true,
        "email": "ava@example.com",
        "id": "string",
        "tags": [
          "string"
        ]
      },
      "success": true,
      "tag": {
        "created": true,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Tag action reference](actions/add-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sequenzy/latest/actions/add-tag).
