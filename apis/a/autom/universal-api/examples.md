# Autom Universal API Examples

These examples use the MindCloud API key and Autom connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage

Retrieves usage details from Autom.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autom/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autom/latest/actions/get-usage?${params}`, {
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
        "name": "Ava Chen",
        "slug": "string"
      },
      "apiKey": {
        "active": true,
        "alias": "string",
        "category": {},
        "expires": {},
        "quotas": {
          "daily": {},
          "monthly": {},
          "total": {},
          "weekly": {}
        }
      },
      "credits": {
        "consumed": 1,
        "given": 1,
        "percentUsed": 1,
        "remaining": "string"
      },
      "period": {
        "end": "2026-05-07T12:00:00.000Z",
        "start": "2026-05-07T12:00:00.000Z"
      },
      "rateLimit": {
        "perMinute": {},
        "perSecond": {}
      },
      "remaining": "string",
      "renewalDate": "2026-05-07T12:00:00.000Z",
      "subscription": {
        "percentUsed": 1,
        "remaining": "string",
        "total": 1,
        "used": 1
      },
      "totalUsed": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Usage action reference](actions/get-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/autom/latest/actions/get-usage).
