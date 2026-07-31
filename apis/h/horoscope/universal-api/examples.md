# Horoscope Universal API Examples

These examples use the MindCloud API key and Horoscope connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Daily Horoscope



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/horoscope/latest/actions/get-daily-horoscope?connectionId=$CONNECTION_ID&sign=aquarius" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sign": "aquarius"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/horoscope/latest/actions/get-daily-horoscope?${params}`, {
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Daily Horoscope action reference](actions/get-daily-horoscope.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/horoscope/latest/actions/get-daily-horoscope).
