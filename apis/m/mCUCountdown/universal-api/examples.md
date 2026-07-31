# MCU Countdown Universal API Examples

These examples use the MindCloud API key and MCU Countdown connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Next MCU Production



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mCUCountdown/latest/actions/get-next-mcu-production?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mCUCountdown/latest/actions/get-next-mcu-production?${params}`, {
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
      "days_until": 1,
      "following_production": {
        "days_until": 1,
        "id": 1,
        "overview": "string",
        "poster_url": "https://example.com",
        "release_date": "string",
        "title": "string",
        "type": "string"
      },
      "id": 1,
      "overview": "string",
      "poster_url": "https://example.com",
      "release_date": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Next MCU Production action reference](actions/get-next-mcu-production.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mCUCountdown/latest/actions/get-next-mcu-production).
