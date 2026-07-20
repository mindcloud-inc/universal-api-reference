# Tumblr Universal API Examples

These examples use the MindCloud API key and Tumblr connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check If Blog Is Followed By Another Blog

Checks whether a Tumblr blog is followed by another blog.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/check-if-blog-is-followed-by-another-blog?connectionId=$CONNECTION_ID&blogIdentifier=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blogIdentifier": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/check-if-blog-is-followed-by-another-blog?${params}`, {
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
      "followedBy": true
    }
  ],
  "meta": {}
}
```

See the full [Check If Blog Is Followed By Another Blog action reference](actions/check-if-blog-is-followed-by-another-blog.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tumblr/latest/actions/check-if-blog-is-followed-by-another-blog).

## Create Post (NPF)

Creates a new Tumblr post using NPF.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/create-post-npf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blogIdentifier": "mindcloudapps",
  "content[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/create-post-npf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blogIdentifier": "mindcloudapps",
    "content[]": "[object Object]"
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
      "displayText": "string",
      "id": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Post (NPF) action reference](actions/create-post-npf.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tumblr/latest/actions/create-post-npf).
