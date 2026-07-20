# Sarbacane Universal API Examples

These examples use the MindCloud API key and Sarbacane connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Credits

Retrieves account credit details from Sarbacane.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-credits?${params}`, {
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
      "count": 1,
      "creditType": "string",
      "expirationDate": "string",
      "subscriptionType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Credits action reference](actions/get-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sarbacane/latest/actions/get-credits).

## Add Campaign Blacklists

Adds blacklist entries to a campaign in Sarbacane.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/add-campaign-blacklists" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/add-campaign-blacklists', {
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Campaign Blacklists action reference](actions/add-campaign-blacklists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sarbacane/latest/actions/add-campaign-blacklists).
