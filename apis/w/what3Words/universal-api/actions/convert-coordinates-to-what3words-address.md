# What3Words: Convert Coordinates to what3words Address

Retrieves a what3words address from coordinates.

```
GET https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/convert-coordinates-to-what3words-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a What3Words `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/convert-coordinates-to-what3words-address?connectionId=$CONNECTION_ID&coordinates=51.521251%2C-0.203586" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "coordinates": "51.521251,-0.203586"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/what3Words/latest/actions/convert-coordinates-to-what3words-address?${params}`, {
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
| `coordinates` | string | yes | Latitude and longitude separated by a comma, for example 51.521251,-0.203586. Example: `51.521251,-0.203586`. |
| `language` | string | no | Supported what3words language code. Defaults to English when omitted. Default: `en`. Example: `en`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | list<string> | no | Response format: json or geojson. One of: `geojson`, `json`. Default: `json`. Example: `json`. |
| `locale` | string | no | Optional locale or script-specific code such as mn_la, zh_tr, or oo_la. Example: `mn_la`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "coordinates": {},
      "country": "string",
      "language": "string",
      "locale": "string",
      "map": "string",
      "nearestPlace": "string",
      "square": {},
      "words": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `coordinates` | object | Latitude and longitude of the square center. |
| `country` | string | ISO 3166-1 alpha-2 country code. |
| `language` | string | Language code of the returned address. |
| `locale` | string | Locale of the returned address, when applicable. |
| `map` | string | URL to view the address on the what3words map. |
| `nearestPlace` | string | Nearest place to the what3words address. |
| `square` | object | Bounds of the 3m x 3m square. |
| `words` | string | The what3words address. |

## Native endpoint

Through the native What3Words API, this operation is `GET /convert-to-3wa` (base URL `https://api.what3words.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-coordinates-to-what3words-address.md) for the provider-specific parameters and requirements.

