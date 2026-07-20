# Email Hippo Universal API Examples

These examples use the MindCloud API key and Email Hippo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Quota Usage

Retrieves quota usage details from Email Hippo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/get-quota-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/get-quota-usage?${params}`, {
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
      "accountId": 1,
      "errorSummary": "string",
      "licenseKey": "string",
      "nextQuotaResetDate": "string",
      "quotaRemaining": 1,
      "quotaUsed": 1,
      "reportedDate": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Quota Usage action reference](actions/get-quota-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/emailHippo/latest/actions/get-quota-usage).
