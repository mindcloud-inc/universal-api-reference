# Rijksmuseum Universal API Examples

These examples use the MindCloud API key and Rijksmuseum connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Dublin Core Object Metadata



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-dublin-core-object-metadata?connectionId=$CONNECTION_ID&metadataObjectId=200107928" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "metadataObjectId": "200107928"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-dublin-core-object-metadata?${params}`, {
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
      "@context": {},
      "@id": "string",
      "@type": "string",
      "creator": {},
      "date": "string",
      "description": "string",
      "identifier": "string",
      "relation": {},
      "rights": {},
      "subject": [
        {}
      ],
      "title": "string",
      "type": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Dublin Core Object Metadata action reference](actions/get-dublin-core-object-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/rijksmuseum/latest/actions/get-dublin-core-object-metadata).
