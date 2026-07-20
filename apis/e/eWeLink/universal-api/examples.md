# eWeLink Universal API Examples

These examples use the MindCloud API key and eWeLink connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Information

Retrieves user information from eWeLink.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-user-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/get-user-information?${params}`, {
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
      "region": "string",
      "user": {
        "accountLevel": 1,
        "apikey": "string",
        "countryCode": "string",
        "email": "ava@example.com",
        "ipCountry": "string",
        "levelExpiredAt": 1,
        "nickname": "Ava Chen",
        "phoneNumber": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get User Information action reference](actions/get-user-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eWeLink/latest/actions/get-user-information).

## Add Group

Creates a new group in eWeLink.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/add-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/add-group', {
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
      "index": 1,
      "itemData": {
        "family": {
          "familyid": "string",
          "roomid": "string"
        },
        "id": "string",
        "mainDeviceId": "string",
        "name": "Ava Chen",
        "params": {}
      },
      "itemType": 1,
      "updatedThingList": [
        {
          "index": 1,
          "itemType": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Group action reference](actions/add-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eWeLink/latest/actions/add-group).
