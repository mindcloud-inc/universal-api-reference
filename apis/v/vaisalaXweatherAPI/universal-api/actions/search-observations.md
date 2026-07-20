# Vaisala Xweather: Search Observations

Finds observations in Vaisala Xweather API.

```
GET https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/search-observations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vaisala Xweather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/search-observations?connectionId=$CONNECTION_ID&query=id%3AKSEA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "id:KSEA"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vaisalaXweatherAPI/latest/actions/search-observations?${params}`, {
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
| `query` | string | yes | Structured Xweather query string for observation search. Example: `id:KSEA`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataSource": "string",
      "id": "string",
      "loc": {},
      "ob": {},
      "obDateTime": "2026-05-07T12:00:00.000Z",
      "obTimestamp": 1,
      "place": {},
      "profile": {},
      "raw": "string"
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
| `ob` | object |  |
| `obDateTime` | date |  |
| `obTimestamp` | number |  |
| `place` | object |  |
| `profile` | object |  |
| `raw` | string |  |

## Native endpoint

Through the native Vaisala Xweather API, this operation is `GET /observations/search` (base URL `https://data.api.xweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-observations.md) for the provider-specific parameters and requirements.

