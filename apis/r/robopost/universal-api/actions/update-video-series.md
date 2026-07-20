# Robopost: Update Video Series

Updates an existing video series in Robopost.

```
PUT https://connect.mindcloud.co/v1/universal/robopost/latest/actions/update-video-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Robopost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/robopost/latest/actions/update-video-series" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "seriesId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/robopost/latest/actions/update-video-series', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "seriesId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `seriesId` | string | yes | The video series ID to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Robopost API, this operation is `PUT /video-series/{series_id}` (base URL `https://public-api.robopost.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-video-series.md) for the provider-specific parameters and requirements.

