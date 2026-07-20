# Bedrijfsdata.nl Universal API Examples

These examples use the MindCloud API key and Bedrijfsdata.nl connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Password Exposure



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/check-password-exposure?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/check-password-exposure?${params}`, {
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
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "monthlyCredits": 1,
      "password": {
        "found": 1,
        "message": "string",
        "success": 1,
        "wrongPassword": 1
      },
      "product": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check Password Exposure action reference](actions/check-password-exposure.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bedrijfsdatanl/latest/actions/check-password-exposure).
