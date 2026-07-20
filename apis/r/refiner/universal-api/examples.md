# Refiner Universal API Examples

These examples use the MindCloud API key and Refiner connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves information about your Refiner account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refiner/latest/actions/get-account-info?${params}`, {
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
      "environments": [
        {}
      ],
      "subscription": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/refiner/latest/actions/get-account-info).

## Add User to Segment

Adds a user to a manual segment in Refiner.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refiner/latest/actions/add-user-to-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "segmentUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refiner/latest/actions/add-user-to-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "segmentUuid": "string"
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
      "contactUuid": "string",
      "message": "string",
      "segmentUid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add User to Segment action reference](actions/add-user-to-segment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/refiner/latest/actions/add-user-to-segment).
