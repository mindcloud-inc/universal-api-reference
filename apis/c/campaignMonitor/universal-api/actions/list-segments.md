# Campaign Monitor: List Segments

Retrieves segments for a Campaign Monitor client.

```
GET https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campaign Monitor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-segments?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campaignMonitor/latest/actions/list-segments?${params}`, {
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
| `clientId` | string | yes | Campaign Monitor client identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listId": "string",
      "segmentId": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `listId` | string | List identifier associated with the segment. |
| `segmentId` | string | Campaign Monitor segment identifier. |
| `title` | string | Segment title. |

## Native endpoint

Through the native Campaign Monitor API, this operation is `GET /clients/:clientId/segments.json` (base URL `https://api.createsend.com/api/v3.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.

