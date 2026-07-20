# Leadfeeder Universal API Examples

These examples use the MindCloud API key and Leadfeeder connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Accounts

Retrieves accounts the user can access in Leadfeeder.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/get-accounts?${params}`, {
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
      "attributes": {
        "name": "Ava Chen",
        "on_trial": true,
        "subscription": "string",
        "subscription_addons": [
          "string"
        ],
        "timezone": "string",
        "website_tracking_status": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Accounts action reference](actions/get-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadfeeder/latest/actions/get-accounts).

## Request Feed Export

Creates a custom feed export request in Leadfeeder.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/request-feed-export" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customFeedId": "all_leads",
  "startDate": "2026-04-01",
  "endDate": "2026-04-13"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadfeeder/latest/actions/request-feed-export', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customFeedId": "all_leads",
    "startDate": "2026-04-01",
    "endDate": "2026-04-13"
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

See the full [Request Feed Export action reference](actions/request-feed-export.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leadfeeder/latest/actions/request-feed-export).
