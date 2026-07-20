# CallTrackingMetrics: Get Tracking Source Details

Retrieves tracking source details from CallTrackingMetrics.

```
GET https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-tracking-source-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-tracking-source-details?connectionId=$CONNECTION_ID&sourceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-tracking-source-details?${params}`, {
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
| `sourceId` | string | yes | The CallTrackingMetrics tracking source ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "description": "string",
      "filterId": 1,
      "geoMode": "string",
      "id": "string",
      "name": "Ava Chen",
      "online": true,
      "position": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `description` | string |  |
| `filterId` | number |  |
| `geoMode` | string |  |
| `id` | string |  |
| `name` | string |  |
| `online` | boolean |  |
| `position` | number |  |
| `url` | string |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `GET /accounts/:accountId/sources/:sourceId.json` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracking-source-details.md) for the provider-specific parameters and requirements.

