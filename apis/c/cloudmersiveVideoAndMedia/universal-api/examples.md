# Cloudmersive Video and Media Universal API Examples

These examples use the MindCloud API key and Cloudmersive Video and Media connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Media Information

Retrieves media information from Cloudmersive Video and Media.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveVideoAndMedia/latest/actions/get-media-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveVideoAndMedia/latest/actions/get-media-information?${params}`, {
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
      "BitRate": 1,
      "Duration": 1,
      "FileFormat": "string",
      "FileFormatFull": "string",
      "Height": 1,
      "Size": 1,
      "StartTime": 1,
      "Successful": true,
      "ValidFileFormats": [
        "string"
      ],
      "Width": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Media Information action reference](actions/get-media-information.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudmersiveVideoAndMedia/latest/actions/get-media-information).
