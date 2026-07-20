# HasData Universal API Examples

These examples use the MindCloud API key and HasData connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage

Retrieves HasData usage and concurrency details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/get-usage?${params}`, {
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
      "data": {
        "availableConcurrency": 1,
        "availableCredits": 1,
        "totalConcurrency": 1,
        "totalCredits": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Usage action reference](actions/get-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hasData/latest/actions/get-usage).
