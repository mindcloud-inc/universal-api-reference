# Robopost: Delete Video Series

Deletes an existing video series from Robopost.

```
DELETE https://connect.mindcloud.co/v1/universal/robopost/latest/actions/delete-video-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Robopost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/robopost/latest/actions/delete-video-series?connectionId=$CONNECTION_ID&seriesId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "seriesId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/robopost/latest/actions/delete-video-series?${params}`, {
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
| `seriesId` | string | yes | The video series ID to delete. |

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

Through the native Robopost API, this operation is `DELETE /video-series/{series_id}` (base URL `https://public-api.robopost.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-video-series.md) for the provider-specific parameters and requirements.

