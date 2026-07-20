# QuickFile Universal API Examples

These examples use the MindCloud API key and QuickFile connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/get-account-details?${params}`, {
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
      "accountNumber": "string",
      "address": "string",
      "backupSchedule": {},
      "baseCurrency": "string",
      "businessType": "string",
      "clientDomain": "string",
      "companyName": "Ava Chen",
      "companyNumber": "string",
      "countryIso": "string",
      "dailyDataTransferLimit": 1,
      "teamMembers": {},
      "tel": "string",
      "vatRegNumber": "string",
      "web": "string",
      "yearEndDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quickFile/latest/actions/get-account-details).

## Create Client



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyName": "Ava Chen"
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
      "clientContactIds": [
        1
      ],
      "clientId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quickFile/latest/actions/create-client).
