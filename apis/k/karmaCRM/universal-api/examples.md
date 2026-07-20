# Karma CRM Universal API Examples

These examples use the MindCloud API key and Karma CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Social Account Types

Retrieves social account types from Karma CRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-social-account-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/list-social-account-types?${params}`, {
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
      "id": 1,
      "index": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Social Account Types action reference](actions/list-social-account-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/karmaCRM/latest/actions/list-social-account-types).

## Apply Campaign

Applies a campaign to a record in Karma CRM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/apply-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignEntry": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/apply-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignEntry": {}
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

See the full [Apply Campaign action reference](actions/apply-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/karmaCRM/latest/actions/apply-campaign).
