# Pitchbox Universal API Examples

These examples use the MindCloud API key and Pitchbox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-my-profile?${params}`, {
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
      "account": {
        "name": "Ava Chen"
      },
      "display_name": "Ava Chen",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_name": "Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pitchbox/latest/actions/get-my-profile).

## Add Campaign Tag



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/add-campaign-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": 1,
  "tag": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/add-campaign-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": 1,
    "tag": 1
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
      "id": 1,
      "tag": {
        "color": "string",
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "taggedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Campaign Tag action reference](actions/add-campaign-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pitchbox/latest/actions/add-campaign-tag).
