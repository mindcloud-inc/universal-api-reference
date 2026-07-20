# Zoho Cliq: List Channel Threads

Retrieves threads from a Zoho Cliq channel.

```
GET https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-channel-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-channel-threads?connectionId=$CONNECTION_ID&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-channel-threads?${params}`, {
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
| `channelId` | string | yes | The ID of the channel whose threads should be retrieved. |
| `state` | string | no | Filter threads by follow state: followed, not_followed, or all. |
| `type` | string | no | Filter threads by status, such as open or closed. |
| `nextToken` | string | no | Use the next token from a previous response to retrieve the next thread page. |
| `limit` | number | no | The maximum number of threads to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "sync_token": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `sync_token` | string |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Zoho Cliq API, this operation is `GET /channels/:channelId/threads` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-threads.md) for the provider-specific parameters and requirements.

