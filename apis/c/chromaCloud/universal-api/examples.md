# Chroma Cloud Universal API Examples

These examples use the MindCloud API key and Chroma Cloud connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get user identity

Retrieves the current user identity from Chroma Cloud.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-user-identity?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/get-user-identity?${params}`, {
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
      "databases": [
        "string"
      ],
      "tenant": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get user identity action reference](actions/get-user-identity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chromaCloud/latest/actions/get-user-identity).

## Add records

Adds records to a collection in Chroma Cloud.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/add-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "ids[]": [
    "string"
  ],
  "embeddings[]": [
    [
      "string"
    ]
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chromaCloud/latest/actions/add-records', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "ids[]": ["string"],
    "embeddings[]": [["string"]]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add records action reference](actions/add-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/chromaCloud/latest/actions/add-records).
