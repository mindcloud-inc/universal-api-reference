# turboSMTP Universal API Examples

These examples use the MindCloud API key and turboSMTP connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Countries

Retrieves available countries from your turboSMTP account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-countries?${params}`, {
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
      "": [
        {
          "currency": "string",
          "flag": "string",
          "iso_code": "string",
          "name": "Ava Chen",
          "phonecode": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Countries action reference](actions/list-countries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/turboSMTP/latest/actions/list-countries).

## Create Alert

Creates a new alert in turboSMTP.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/create-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "turbosmtp-alert-attempt2@example.com",
  "percentage": "80"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/create-alert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "turbosmtp-alert-attempt2@example.com",
    "percentage": "80"
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
      "email": "ava@example.com",
      "id": 1,
      "percentage": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Alert action reference](actions/create-alert.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/turboSMTP/latest/actions/create-alert).
