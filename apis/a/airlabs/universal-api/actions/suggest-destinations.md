# Airlabs: Suggest Destinations

Finds destination suggestions in Airlabs by search query.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/suggest-destinations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/suggest-destinations?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/suggest-destinations?${params}`, {
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
| `query` | string | yes | Part of the destination name, airport, city, or country. AirLabs documents 3 to 30 characters. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "airports": [
        {}
      ],
      "airports_by_cities": [
        {}
      ],
      "airports_by_countries": [
        {}
      ],
      "cities": [
        {}
      ],
      "cities_by_airports": [
        {}
      ],
      "cities_by_countries": [
        {}
      ],
      "countries": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airports` | array<object> | Matching airports. |
| `airports_by_cities` | array<object> | Airports matched by city search. |
| `airports_by_countries` | array<object> | Airports matched by country search. |
| `cities` | array<object> | Matching cities. |
| `cities_by_airports` | array<object> | Cities matched by airport search. |
| `cities_by_countries` | array<object> | Cities matched by country search. |
| `countries` | array<object> | Matching countries. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /suggest` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-destinations.md) for the provider-specific parameters and requirements.

