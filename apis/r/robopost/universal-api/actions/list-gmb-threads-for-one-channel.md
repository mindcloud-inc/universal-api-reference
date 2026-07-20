# Robopost: List GMB Threads for One Channel

Retrieves Google Business threads for one Robopost channel.

```
GET https://connect.mindcloud.co/v1/universal/robopost/latest/actions/list-gmb-threads-for-one-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Robopost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/robopost/latest/actions/list-gmb-threads-for-one-channel?connectionId=$CONNECTION_ID&limit=25&offset=0&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/robopost/latest/actions/list-gmb-threads-for-one-channel?${params}`, {
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
| `channelId` | string | yes | The Robopost channel ID. This endpoint only works for Google Business channels. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Robopost API, this operation is `GET /social_inbox_items/channels/{channel_id}/gmb/threads` (base URL `https://public-api.robopost.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-gmb-threads-for-one-channel.md) for the provider-specific parameters and requirements.

