# COVID-19 JHU CSSE: List Location Lookup Table

Retrieves the COVID-19 location lookup rows.

```
GET https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-location-lookup-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a COVID-19 JHU CSSE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-location-lookup-table?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cOVID19JHUCSSE/latest/actions/list-location-lookup-table?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "admin2": "string",
      "code3": 1,
      "combinedKey": "string",
      "countryRegion": "string",
      "fips": 1,
      "iso2": "string",
      "iso3": "string",
      "lat": 1,
      "long": 1,
      "population": 1,
      "provinceState": "string",
      "uid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin2` | string | County or equivalent local administrative area. |
| `code3` | number | ISO numeric country code. |
| `combinedKey` | string | Combined source location label. |
| `countryRegion` | string | Country or region name. |
| `fips` | number | FIPS code when provided. |
| `iso2` | string | ISO alpha-2 country code. |
| `iso3` | string | ISO alpha-3 country code. |
| `lat` | number | Latitude for the location. |
| `long` | number | Longitude for the location. |
| `population` | number | Population for the location when provided. |
| `provinceState` | string | Province or state name when provided. |
| `uid` | number | JHU location UID. |

## Native endpoint

Through the native COVID-19 JHU CSSE API, this operation is `GET /UID_ISO_FIPS_LookUp_Table.csv` (base URL `https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-location-lookup-table.md) for the provider-specific parameters and requirements.

