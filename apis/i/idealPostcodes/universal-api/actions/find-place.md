# Ideal Postcodes: Find Place

Finds place suggestions in Ideal Postcodes by text query.

```
GET https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/find-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ideal Postcodes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/find-place?connectionId=$CONNECTION_ID&query=london" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "london"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/find-place?${params}`, {
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
| `query` | string | yes | Place query string. Default: `london`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `countryIso` | string | no | Comma-separated ISO 3166-1 alpha-3 country codes to filter by. |
| `biasCountryIso` | string | no | Comma-separated ISO 3166-1 alpha-3 country codes to bias results toward. |
| `biasLonlat` | string | no | Longitude, latitude, and radius bias in the form lon,lat,radius. |
| `biasIp` | boolean | no | Set to true to bias results using the request IP location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryIso": "string",
      "descriptiveName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryIso` | string |  |
| `descriptiveName` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Ideal Postcodes API, this operation is `GET /places` (base URL `https://api.ideal-postcodes.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-place.md) for the provider-specific parameters and requirements.

