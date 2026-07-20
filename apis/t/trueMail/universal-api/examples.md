# TrueMail Universal API Examples

These examples use the MindCloud API key and TrueMail connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Usage

Retrieves account usage details from TrueMail.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/check-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/check-usage?${params}`, {
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
      "credits": {
        "locked": 1,
        "total": 1
      },
      "period": {
        "end": "string",
        "start": "string"
      },
      "plan": "string",
      "rateLimit": {
        "limit": 1
      },
      "validationTypes": {
        "mx": {
          "available": true,
          "credits": 1
        },
        "smtp": {
          "available": true,
          "credits": 1,
          "upgradeRequired": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Check Usage action reference](actions/check-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trueMail/latest/actions/check-usage).

## Create Filter

Creates a new blocklist filter in TrueMail.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/create-filter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filterType": "0",
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trueMail/latest/actions/create-filter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filterType": "0",
    "value": "string"
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
      "filter": {
        "createdAt": "string",
        "filterType": "string",
        "id": 1,
        "reason": "string",
        "updatedAt": "string",
        "userId": 1,
        "value": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Filter action reference](actions/create-filter.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trueMail/latest/actions/create-filter).
