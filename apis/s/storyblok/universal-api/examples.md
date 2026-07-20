# Storyblok Universal API Examples

These examples use the MindCloud API key and Storyblok connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Space

Retrieves the current space from Storyblok.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-current-space?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-current-space?${params}`, {
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
      "space": {
        "domain": "string",
        "id": 1,
        "languageCodes": [
          "string"
        ],
        "name": "Ava Chen",
        "version": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current Space action reference](actions/get-current-space.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/storyblok/latest/actions/get-current-space).
