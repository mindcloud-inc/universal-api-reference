# Směnné kurzy ČNB Universal API Examples

These examples use the MindCloud API key and Směnné kurzy ČNB connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get CNB Czeonia Daily

Retrieves the last valid CZEONIA rate from Směnné kurzy ČNB.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-czeonia-daily?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smnnKurzyNB/latest/actions/get-cnb-czeonia-daily?${params}`, {
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
      "czeoniaDaily": {
        "rate": 1,
        "validFor": "string",
        "volumeInCZKmio": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Get CNB Czeonia Daily action reference](actions/get-cnb-czeonia-daily.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/smnnKurzyNB/latest/actions/get-cnb-czeonia-daily).
