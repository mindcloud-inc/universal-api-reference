# Finnish Railway Traffic: List active passenger information messages

Retrieves active passenger information messages from Finnish Railway Traffic.

```
GET https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-active-passenger-information-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish Railway Traffic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-active-passenger-information-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-active-passenger-information-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "audio": {},
      "id": "string",
      "stations": [
        "string"
      ],
      "trainDepartureDate": "2026-05-07T12:00:00.000Z",
      "trainNumber": 1,
      "version": 1,
      "video": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audio` | object |  |
| `id` | string |  |
| `stations` | array<string> |  |
| `trainDepartureDate` | date |  |
| `trainNumber` | number |  |
| `version` | number |  |
| `video` | object |  |

## Native endpoint

Through the native Finnish Railway Traffic API, this operation is `GET /api/v1/passenger-information/active` (base URL `https://rata.digitraffic.fi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-passenger-information-messages.md) for the provider-specific parameters and requirements.

