# NASA Image and Video Library Universal API Examples

These examples use the MindCloud API key and NASA Image and Video Library connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Album Contents

Retrieves album contents from NASA Image and Video Library.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-album-contents?connectionId=$CONNECTION_ID&albumName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "albumName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nASAImageAndVideoLibrary/latest/actions/get-album-contents?${params}`, {
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
      "collection": {
        "href": "string",
        "items": [
          {
            "data": [
              {
                "center": "string",
                "date_created": "2026-05-07T12:00:00.000Z",
                "description": "string",
                "keywords": [
                  "string"
                ],
                "location": "string",
                "media_type": "string",
                "nasa_id": "string",
                "photographer": "string",
                "title": "string"
              }
            ],
            "href": "string",
            "links": [
              {}
            ]
          }
        ],
        "links": [
          {}
        ],
        "metadata": {
          "total_hits": 1
        },
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Album Contents action reference](actions/get-album-contents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nASAImageAndVideoLibrary/latest/actions/get-album-contents).
