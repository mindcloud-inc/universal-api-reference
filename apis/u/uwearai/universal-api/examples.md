# Uwear.ai Universal API Examples

These examples use the MindCloud API key and Uwear.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Clothing Items

Retrieves clothing items from Uwear.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-all-clothing-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-all-clothing-items?${params}`, {
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
      "current_page": 1,
      "data": [
        {}
      ],
      "max_page": 1,
      "total_count": 1
    }
  ],
  "meta": {}
}
```

See the full [Get All Clothing Items action reference](actions/get-all-clothing-items.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uwearai/latest/actions/get-all-clothing-items).

## Create Avatar

Creates an avatar generation in Uwear.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "num_images": "1",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/create-avatar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "num_images": "1",
    "prompt": "string"
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
      "created_at": "string",
      "feature_name": "Ava Chen",
      "generation_id": 1,
      "generation_results": [
        {}
      ],
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Avatar action reference](actions/create-avatar.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uwearai/latest/actions/create-avatar).
