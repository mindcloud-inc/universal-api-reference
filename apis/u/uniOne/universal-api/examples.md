# UniOne Universal API Examples

These examples use the MindCloud API key and UniOne connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get System Info

Retrieves account and usage details from UniOne.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-system-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/get-system-info?${params}`, {
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
      "accounting": {
        "emailsIncluded": 1,
        "emailsSent": 1,
        "periodEnd": "string",
        "periodStart": "string",
        "validationsIncluded": 1,
        "validationsUsed": 1
      },
      "email": "ava@example.com",
      "status": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get System Info action reference](actions/get-system-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uniOne/latest/actions/get-system-info).

## Add Suppression

Adds an email address to UniOne's suppression list.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/add-suppression" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "wizard-suppression-20260402@mindcloud.co",
  "cause": "unsubscribed"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/add-suppression', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "wizard-suppression-20260402@mindcloud.co",
    "cause": "unsubscribed"
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

See the full [Add Suppression action reference](actions/add-suppression.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uniOne/latest/actions/add-suppression).
