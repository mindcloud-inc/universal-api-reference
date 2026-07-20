# EyeLevel.ai Universal API Examples

These examples use the MindCloud API key and EyeLevel.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Customer

Retrieves account information from EyeLevel.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-customer?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/get-customer?${params}`, {
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
      "customer": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Customer action reference](actions/get-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eyeLevelai/latest/actions/get-customer).

## Add Bucket To Group

Adds a bucket to a group in EyeLevel.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/add-bucket-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": 1,
  "bucketId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eyeLevelai/latest/actions/add-bucket-to-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": 1,
    "bucketId": 1
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Bucket To Group action reference](actions/add-bucket-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/eyeLevelai/latest/actions/add-bucket-to-group).
