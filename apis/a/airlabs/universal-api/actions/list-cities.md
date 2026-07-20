# Airlabs: List Cities

Retrieves city database records from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-cities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-cities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-cities?${params}`, {
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
| `cityCode` | string | no | Filter by IATA city code. |
| `countryCode` | string | no | Filter by country ISO 2 code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city_code": "string",
      "country_code": "string",
      "lat": 1,
      "lng": 1,
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city_code` | string | City code. |
| `country_code` | string | Country ISO 2 code. |
| `lat` | number | City latitude. |
| `lng` | number | City longitude. |
| `name` | string | City name. |
| `type` | string | AirLabs city record type. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /cities` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cities.md) for the provider-specific parameters and requirements.

