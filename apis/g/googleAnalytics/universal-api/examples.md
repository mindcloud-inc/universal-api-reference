# Google Analytics Universal API Examples

These examples use the MindCloud API key and Google Analytics connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Account Summaries



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-account-summaries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-account-summaries?${params}`, {
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
      "accountSummaries": [
        {}
      ],
      "nextPageToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Account Summaries action reference](actions/list-account-summaries.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleAnalytics/latest/actions/list-account-summaries).
