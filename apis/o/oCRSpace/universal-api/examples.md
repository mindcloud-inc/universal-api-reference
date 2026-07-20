# OCRSpace Universal API Examples

These examples use the MindCloud API key and OCRSpace connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Parse Image URL



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/parse-image-url?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oCRSpace/latest/actions/parse-image-url?${params}`, {
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
      "IsErroredOnProcessing": true,
      "OCRExitCode": 1,
      "ParsedResults": [
        {}
      ],
      "ProcessingTimeInMilliseconds": "string",
      "SearchablePDFURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Parse Image URL action reference](actions/parse-image-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oCRSpace/latest/actions/parse-image-url).
