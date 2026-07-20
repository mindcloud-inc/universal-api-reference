# Straker Verify Universal API Examples

These examples use the MindCloud API key and Straker Verify connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Token Balance

Retrieves your token balance from Straker Verify.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strakerVerify/latest/actions/get-token-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strakerVerify/latest/actions/get-token-balance?${params}`, {
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

See the full [Get Token Balance action reference](actions/get-token-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/strakerVerify/latest/actions/get-token-balance).
