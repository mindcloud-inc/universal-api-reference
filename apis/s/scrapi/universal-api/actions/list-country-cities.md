# Scrapi: List Country Cities

Retrieves supported proxy cities for a country from Scrapi.

```
GET https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/list-country-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/list-country-cities?connectionId=$CONNECTION_ID&countryKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapi/latest/actions/list-country-cities?${params}`, {
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
| `countryKey` | string | yes | Country key used to look up supported cities. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Scrapi API, this operation is `GET /v1/countries/{countryKey}/cities` (base URL `https://api.scrapi.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-country-cities.md) for the provider-specific parameters and requirements.

