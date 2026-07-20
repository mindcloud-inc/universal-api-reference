# Postalytics Universal API Examples

These examples use the MindCloud API key and Postalytics connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Account

Retrieves your authenticated Postalytics account details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-my-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/get-my-account?${params}`, {
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
      "account_id": 1,
      "address_city": "string",
      "address_state": "string",
      "address_street": "string",
      "address_zip": "string",
      "company": "string",
      "created_date": "string",
      "email_address": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "phone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get My Account action reference](actions/get-my-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postalytics/latest/actions/get-my-account).

## Create Suppression List

Creates a suppression list in Postalytics.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/create-suppression-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postalytics/latest/actions/create-suppression-list', {
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
      "Country": "string",
      "CreationDate": "string",
      "Id": 1,
      "Name": "Ava Chen",
      "Total": 1,
      "Type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Suppression List action reference](actions/create-suppression-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postalytics/latest/actions/create-suppression-list).
