# imgix Universal API Examples

These examples use the MindCloud API key and imgix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sources

Retrieves sources from imgix.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imgix/latest/actions/list-sources?${params}`, {
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
      "data": [
        {
          "attributes": {
            "deployment": {
              "type": "string"
            },
            "deploymentStatus": "string",
            "enabled": true,
            "name": "Ava Chen"
          },
          "id": "string",
          "type": "string"
        }
      ],
      "meta": {
        "pagination": {
          "currentPage": 1,
          "hasNextPage": true,
          "totalRecords": 1
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [List Sources action reference](actions/list-sources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/imgix/latest/actions/list-sources).

## Add Asset From Origin

Adds an asset from origin to imgix.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/add-asset-from-origin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "originPath": "string",
  "sourceId": "69de49d580720625c04f9162"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imgix/latest/actions/add-asset-from-origin', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "originPath": "string",
    "sourceId": "69de49d580720625c04f9162"
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
      "data": {
        "attributes": {
          "contentType": "string",
          "mediaKind": "string",
          "originPath": "string",
          "sourceId": "string"
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Add Asset From Origin action reference](actions/add-asset-from-origin.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/imgix/latest/actions/add-asset-from-origin).
