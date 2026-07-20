# What3Words: Suggest what3words Addresses

Finds suggested what3words addresses from text input.

```
GET https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/suggest-what3words-addresses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a What3Words `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/suggest-what3words-addresses?connectionId=$CONNECTION_ID&input=filled.count.s" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "filled.count.s"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/suggest-what3words-addresses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input` | string | yes | Full or partial what3words address. At minimum, use the first two complete words plus one character from the third word. Example: `filled.count.s`. |
| `focus` | string | no | Latitude and longitude used to prioritize nearby suggestions, for example 51.521251,-0.203586. Example: `51.521251,-0.203586`. |
| `nResults` | number | no | Number of suggestions to return. Values over 100 are truncated to 100. Default: `3`. Example: `3`. |
| `language` | string | no | Preferred language or locale to guide autosuggest. Required for voice input modes. Default: `en`. Example: `en`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nFocusResults` | number | no | Number of top suggestions strongly biased toward the focus coordinate. Example: `3`. |
| `clipToCountry` | string | no | Restrict suggestions to comma-separated ISO 3166-1 alpha-2 country codes, for example GB,US. Example: `GB,US`. |
| `clipToCircle` | string | no | Restrict suggestions to latitude,longitude,kilometres, for example 51.4243877,-0.3474524,10. Example: `51.4243877,-0.3474524,10`. |
| `clipToBoundingBox` | string | no | Restrict suggestions to southwest latitude, southwest longitude, northeast latitude, northeast longitude. Example: `51.515900,-0.212517,51.527649,-0.191746`. |
| `clipToPolygon` | string | no | Restrict suggestions to a closed polygon of comma-separated latitude/longitude pairs, up to 25 pairs. Example: `51.521,-0.343,52.6,2.3324,54.234,8.343,51.521,-0.343`. |
| `locale` | string | no | Optional locale or script-specific code. If language is also provided, both values must match. Example: `mn_la`. |
| `inputType` | list<string> | no | Input mode. Text is the default; voice modes require language. One of: `generic-voice`, `nmdp-asr`, `speechmatics`, `text`, `vin-big-data`, `vocon-hybrid`. Default: `text`. Example: `text`. |
| `preferLand` | boolean | no | Prefer land-based suggestions. Enabled by default by what3words. Default: `true`. Example: `true`. |
| `format` | list<string> | no | Response format: json or geojson. One of: `geojson`, `json`. Default: `json`. Example: `json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "distanceToFocusKm": 1,
      "language": "string",
      "locale": "string",
      "nearestPlace": "string",
      "rank": 1,
      "words": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | ISO 3166-1 alpha-2 country code for the suggestion. |
| `distanceToFocusKm` | number | Distance in kilometers from the focus coordinate, when focus is supplied. |
| `language` | string | Language code for the suggestion. |
| `locale` | string | Locale for the suggestion, when applicable. |
| `nearestPlace` | string | Nearest place for the suggested address. |
| `rank` | number | Relative rank of the suggestion. |
| `words` | string | Suggested what3words address. |

## Native endpoint

Through the native What3Words API, this operation is `GET /autosuggest` (base URL `https://api.what3words.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-what3words-addresses.md) for the provider-specific parameters and requirements.

