# Vaisala Xweather: Search Places

Finds places in Vaisala Xweather API.

```
GET https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/search-places
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaisala Xweather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/search-places?connectionId=$CONNECTION_ID&query=name%3Aseattle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "name:seattle"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/search-places?${params}`, {
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
| `query` | string | yes | Structured Xweather query string, for example `name:seattle`. Example: `name:seattle`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "loc": {},
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
| `place` | object |  |
| `profile` | object |  |

## Native endpoint

Through the native Vaisala Xweather API, this operation is `GET /places/search` (base URL `https://data.api.xweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-places.md) for the provider-specific parameters and requirements.

