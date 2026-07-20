# DataForB2B Universal API Examples

These examples use the MindCloud API key and DataForB2B connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves account details from DataForB2B.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/get-account?${params}`, {
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
      "credits": 1,
      "valid": true
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataForB2B/latest/actions/get-account).

## Add Profiles To Monitor

Adds profiles to monitoring in DataForB2B.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/add-profiles-to-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileIds": [
    "https://www.linkedin.com/in/satyanadella/"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/add-profiles-to-monitor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileIds": ["https://www.linkedin.com/in/satyanadella/"]
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
      "added": 1,
      "already_monitored": 1,
      "errors": [
        {}
      ],
      "failed": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Profiles To Monitor action reference](actions/add-profiles-to-monitor.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dataForB2B/latest/actions/add-profiles-to-monitor).
