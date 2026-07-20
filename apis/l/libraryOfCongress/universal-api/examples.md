# Library of Congress Universal API Examples

These examples use the MindCloud API key and Library of Congress connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Collection

Retrieves a Library of Congress digital collection.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "collectionSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/get-collection?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Collection action reference](actions/get-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/libraryOfCongress/latest/actions/get-collection).
