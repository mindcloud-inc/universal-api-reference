# Rownd Data Privacy Universal API Examples

These examples use the MindCloud API key and Rownd Data Privacy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Sample User Profile Data



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/get-sample-user-profile-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/get-sample-user-profile-data?${params}`, {
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
      "data": {},
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Sample User Profile Data action reference](actions/get-sample-user-profile-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rowndDataPrivacy/latest/actions/get-sample-user-profile-data).

## Create Group



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rowndDataPrivacy/latest/actions/create-group', {
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
      "admission_policy": "string",
      "id": "string",
      "member_count": 1,
      "meta": {},
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Group action reference](actions/create-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rowndDataPrivacy/latest/actions/create-group).
