# Robots for Power BI: Disable playlist

Disables a playlist in Robots for Power BI.

```
PUT https://connect.mindcloud.co/v1/universal/robotsForPowerBI/latest/actions/disable-playlist
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Robots for Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/robotsForPowerBI/latest/actions/disable-playlist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "00000000-0000-0000-0000-000000000000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/robotsForPowerBI/latest/actions/disable-playlist', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "00000000-0000-0000-0000-000000000000"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | PowerBI Robots playlist UUID to disable. Example: `00000000-0000-0000-0000-000000000000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "message": "string",
      "ok": true,
      "playlist": {
        "cronDescription": "string",
        "cronExpression": "string",
        "id": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Provider error code when the operation does not succeed. |
| `message` | string | Provider error message when available. |
| `ok` | boolean | Whether the playlist operation succeeded. |
| `playlist` | object | Playlist returned by PowerBI Robots when available. |
| `playlist.cronDescription` | string | Human-readable playlist schedule. |
| `playlist.cronExpression` | string | Playlist schedule expression. |
| `playlist.id` | string | Playlist UUID. |
| `playlist.title` | string | Playlist title. |

## Native endpoint

Through the native Robots for Power BI API, this operation is `POST /api/v1/playlist.disable` (base URL `https://www.powerbitiles.com/PBIRobots`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-playlist.md) for the provider-specific parameters and requirements.

