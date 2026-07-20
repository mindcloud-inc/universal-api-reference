# Zoho Survey Universal API Examples

These examples use the MindCloud API key and Zoho Survey connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get OAuth User Info

Retrieves connected Zoho account user info for Zoho Survey.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSurvey/latest/actions/get-oauth-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSurvey/latest/actions/get-oauth-user-info?${params}`, {
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
      "Display_Name": "Ava Chen",
      "Email": "ava@example.com",
      "First_Name": "Ava",
      "Last_Name": "Chen",
      "ZUID": 1
    }
  ],
  "meta": {}
}
```

See the full [Get OAuth User Info action reference](actions/get-oauth-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoSurvey/latest/actions/get-oauth-user-info).
