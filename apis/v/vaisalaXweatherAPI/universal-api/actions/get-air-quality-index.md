# Vaisala Xweather: Get Air Quality Index

Retrieves air quality index data from Vaisala Xweather API.

```
GET https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-air-quality-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaisala Xweather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-air-quality-index?connectionId=$CONNECTION_ID&id=seattle%2Cwa" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "seattle,wa"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/get-air-quality-index?${params}`, {
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
| `id` | string | yes | Location, place identifier, or latitude/longitude. Example: `seattle,wa`. |

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
      "place": {},
      "profile": {}
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
| `profile` | object |  |

## Native endpoint

Through the native Vaisala Xweather API, this operation is `GET /airquality/index/:id` (base URL `https://data.api.xweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-air-quality-index.md) for the provider-specific parameters and requirements.

