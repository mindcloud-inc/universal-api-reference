# VAT Comply: List Countries

Retrieves a list of countries from VAT Comply.

```
GET https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/list-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VAT Comply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/list-countries?${params}`, {
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
| `search` | string | no | Filter countries by a search string. |
| `region` | string | no | Filter countries by region. |
| `subregion` | string | no | Filter countries by subregion. |
| `currency` | string | no | Filter countries by currency code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capital": "string",
      "currency": "string",
      "emoji": "string",
      "iso2": "string",
      "iso3": "string",
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "numeric_code": 1,
      "phone_code": "string",
      "region": "string",
      "subregion": "string",
      "tld": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capital` | string |  |
| `currency` | string |  |
| `emoji` | string |  |
| `iso2` | string |  |
| `iso3` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `numeric_code` | number |  |
| `phone_code` | string |  |
| `region` | string |  |
| `subregion` | string |  |
| `tld` | string |  |

## Native endpoint

Through the native VAT Comply API, this operation is `GET /countries` (base URL `https://api.vatcomply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-countries.md) for the provider-specific parameters and requirements.

