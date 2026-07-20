# FullSession Universal API Examples

These examples use the MindCloud API key and FullSession connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Website Sessions

Retrieves website visitor sessions from FullSession.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fullSession/latest/actions/list-website-sessions?connectionId=$CONNECTION_ID&customerId=string&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "string",
  "siteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fullSession/latest/actions/list-website-sessions?${params}`, {
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
      "activeTime": 1,
      "browser": "string",
      "browserFullVersion": "string",
      "city": "string",
      "country": "string",
      "countryCode": "string",
      "device": "string",
      "duration": 1,
      "endTime": 1,
      "exitPage": "string",
      "landingPage": "string",
      "os": "string",
      "pages": [
        {
          "fullPath": "string"
        }
      ],
      "referrer": "string",
      "startTime": 1,
      "userId": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Website Sessions action reference](actions/list-website-sessions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fullSession/latest/actions/list-website-sessions).
