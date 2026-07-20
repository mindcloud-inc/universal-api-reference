# AccuWeather Universal API Examples

These examples use the MindCloud API key and AccuWeather connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Supported Languages

Lists the supported languages in AccuWeather.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-supported-languages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/list-supported-languages?${params}`, {
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
      "DisplayName": "Ava Chen",
      "ID": 1,
      "ISO": "string",
      "LanguageType": 1,
      "LocalizedName": "Ava Chen",
      "MicroSoftCode": "string",
      "MicroSoftName": "Ava Chen",
      "Name": "Ava Chen",
      "TimeStamp": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Supported Languages action reference](actions/list-supported-languages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/accuWeather/latest/actions/list-supported-languages).
