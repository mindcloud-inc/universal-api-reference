# Finnish Railway Traffic: List trackwork notifications

Retrieves trackwork notifications in JSON from Finnish Railway Traffic.

```
GET https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-trackwork-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish Railway Traffic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-trackwork-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/list-trackwork-notifications?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "organization": "string",
      "state": "string",
      "trafficSafetyPlan": {},
      "version": 1,
      "workParts": [
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
| `created` | date |  |
| `id` | string |  |
| `modified` | date |  |
| `organization` | string |  |
| `state` | string |  |
| `trafficSafetyPlan` | object |  |
| `version` | number |  |
| `workParts` | array<object> |  |

## Native endpoint

Through the native Finnish Railway Traffic API, this operation is `GET /api/v1/trackwork-notifications.json` (base URL `https://rata.digitraffic.fi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-trackwork-notifications.md) for the provider-specific parameters and requirements.

