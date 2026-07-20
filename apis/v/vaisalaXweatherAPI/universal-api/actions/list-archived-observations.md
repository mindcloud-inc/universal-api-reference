# Vaisala Xweather: List Archived Observations

Retrieves archived observations from Vaisala Xweather API.

```
GET https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-archived-observations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaisala Xweather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-archived-observations?connectionId=$CONNECTION_ID&id=seattle%2Cwa&from=2026-03-29" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "seattle,wa",
  "from": "2026-03-29"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/list-archived-observations?${params}`, {
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
| `id` | string | yes | Location, station identifier, postal code, or latitude/longitude. Example: `seattle,wa`. |
| `from` | date | yes | Archive date to retrieve in YYYY-MM-DD format. Example: `2026-03-29`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataSource": "string",
      "id": "string",
      "loc": {},
      "periods": [
        {}
      ],
      "place": {},
      "profile": {},
      "relativeTo": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataSource` | string |  |
| `id` | string |  |
| `loc` | object |  |
| `periods` | array<object> |  |
| `place` | object |  |
| `profile` | object |  |
| `relativeTo` | object |  |

## Native endpoint

Through the native Vaisala Xweather API, this operation is `GET /observations/archive/:id` (base URL `https://data.api.xweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-archived-observations.md) for the provider-specific parameters and requirements.

