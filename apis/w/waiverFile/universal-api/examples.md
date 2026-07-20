# WaiverFile Universal API Examples

These examples use the MindCloud API key and WaiverFile connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Site Details

Retrieves site details from WaiverFile.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-site-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/get-site-details?${params}`, {
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
      "_doc": {},
      "_labels": [
        {}
      ],
      "_WPObjectStatus": 1,
      "me": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Site Details action reference](actions/get-site-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/waiverFile/latest/actions/get-site-details).

## Create Edit Check-In Subscription

Creates an edit check-in subscription in WaiverFile.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/create-edit-check-in-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/create-edit-check-in-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com"
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

See the full [Create Edit Check-In Subscription action reference](actions/create-edit-check-in-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/waiverFile/latest/actions/create-edit-check-in-subscription).
