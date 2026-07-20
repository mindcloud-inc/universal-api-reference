# turboSMTP: List States by Country

Retrieves states for a country from turboSMTP.

```
GET https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-states-by-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-states-by-country?connectionId=$CONNECTION_ID&isoCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "isoCode": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/list-states-by-country?${params}`, {
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
| `isoCode` | string | yes | Two-letter country ISO code. Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country_code": "string",
      "iso_code": "string",
      "name": "Ava Chen",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_code` | string |  |
| `iso_code` | string |  |
| `name` | string |  |
| `type` | number |  |

## Native endpoint

Through the native turboSMTP API, this operation is `GET /meta/state/{isoCode}` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-states-by-country.md) for the provider-specific parameters and requirements.

