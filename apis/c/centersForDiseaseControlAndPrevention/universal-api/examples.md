# Centers for Disease Control and Prevention Universal API Examples

These examples use the MindCloud API key and Centers for Disease Control and Prevention connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Media

Retrieves media from CDC Content Services by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/get-media?connectionId=$CONNECTION_ID&mediaId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centersForDiseaseControlAndPrevention/latest/actions/get-media?${params}`, {
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
      "dateModified": "2026-05-07T12:00:00.000Z",
      "datePublished": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "language": {},
      "mediaType": "string",
      "name": "Ava Chen",
      "source": {},
      "sourceUrl": "https://example.com",
      "tags": [
        {}
      ],
      "targetUrl": "https://example.com",
      "thumbnailUrl": "https://example.com",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Media action reference](actions/get-media.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/centersForDiseaseControlAndPrevention/latest/actions/get-media).
