# ScrapingDog Universal API Examples

These examples use the MindCloud API key and ScrapingDog connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details

Retrieves account details from ScrapingDog.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-account-details?${params}`, {
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
      "concurrencyLimit": 1,
      "email": "ava@example.com",
      "linkedinConcurrencyLimit": 1,
      "linkedinThreadCount": 1,
      "pack": "string",
      "packType": "string",
      "requestLimit": 1,
      "requestUsed": 1,
      "threadCount": 1,
      "username": "Ava Chen",
      "validity": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapingDog/latest/actions/get-account-details).
