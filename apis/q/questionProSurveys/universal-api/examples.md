# QuestionPro Surveys Universal API Examples

These examples use the MindCloud API key and QuestionPro Surveys connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Organization



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=1234567" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1234567"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-organization?${params}`, {
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
      "accountRepEmail": "ava@example.com",
      "dashboardUserCount": 1,
      "license": "string",
      "name": "Ava Chen",
      "organizationID": 1,
      "primaryAccountID": 1,
      "primaryAccountUsername": "Ava Chen",
      "shortUrl": "https://example.com",
      "smtpRelay": "string",
      "styleSheet": "string",
      "usage": {},
      "userCount": 1,
      "welcomeHTML": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Organization action reference](actions/get-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/questionProSurveys/latest/actions/get-organization).
