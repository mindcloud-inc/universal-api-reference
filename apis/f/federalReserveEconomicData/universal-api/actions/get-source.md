# Federal Reserve Economic Data: Get Source

Retrieves a source from Federal Reserve Economic Data.

```
GET https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Federal Reserve Economic Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-source?connectionId=$CONNECTION_ID&source_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "source_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/federalReserveEconomicData/latest/actions/get-source?${params}`, {
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
| `source_id` | number | yes | The id for a source. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "realtime_end": "2026-05-07T12:00:00.000Z",
      "realtime_start": "2026-05-07T12:00:00.000Z",
      "sources": [
        {
          "id": 1,
          "link": "https://example.com",
          "name": "Ava Chen",
          "realtime_end": "2026-05-07T12:00:00.000Z",
          "realtime_start": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `realtime_end` | date |  |
| `realtime_start` | date |  |
| `sources[].id` | number |  |
| `sources[].link` | string |  |
| `sources[].name` | string |  |
| `sources[].realtime_end` | date |  |
| `sources[].realtime_start` | date |  |

## Native endpoint

Through the native Federal Reserve Economic Data API, this operation is `GET /fred/source` (base URL `https://api.stlouisfed.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-source.md) for the provider-specific parameters and requirements.

