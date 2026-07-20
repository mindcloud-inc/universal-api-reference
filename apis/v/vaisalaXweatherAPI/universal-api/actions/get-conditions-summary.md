# Vaisala Xweather: Get Conditions Summary

Retrieves conditions summary data from Vaisala Xweather API.

```
GET https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-conditions-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaisala Xweather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-conditions-summary?connectionId=$CONNECTION_ID&id=seattle%2Cwa&from=2026-03-25" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "seattle,wa",
  "from": "2026-03-25"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-conditions-summary?${params}`, {
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
| `from` | date | yes | Start date for the summary window in YYYY-MM-DD format. Example: `2026-03-25`. |
| `to` | date | no | End date for the summary window in YYYY-MM-DD format. Example: `2026-03-29`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "loc": {},
      "periods": [
        {}
      ],
      "place": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `loc` | object |  |
| `periods` | array<object> |  |
| `place` | object |  |

## Native endpoint

Through the native Vaisala Xweather API, this operation is `GET /conditions/summary/:id` (base URL `https://data.api.xweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conditions-summary.md) for the provider-specific parameters and requirements.

