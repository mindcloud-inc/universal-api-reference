# Zoho Cliq: List Channels

Retrieves Zoho Cliq channels by filters.

```
GET https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-channels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/list-channels?${params}`, {
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
| `name` | string | no | Filter channels by name. |
| `status` | string | no | Filter channels by status: created, pending, or archived. |
| `limit` | number | no | The number of channels to retrieve. Maximum 100. |
| `level` | string | no | Filter channels by level: organization, team, private, or external. |
| `modifiedBefore` | string | no | Only include channels whose last message was sent before this time. |
| `modifiedAfter` | string | no | Only include channels whose last message was sent after this time. |
| `createdBefore` | string | no | Only include channels created before this time. |
| `createdAfter` | string | no | Only include channels created after this time. |
| `channelIds` | string | no | Comma-separated channel IDs to retrieve. |
| `chatIds` | string | no | Comma-separated channel chat IDs to retrieve. |
| `teamIds` | string | no | Comma-separated team IDs whose channels should be retrieved. |
| `createdBy` | string | no | Filter channels by creator email or user ID. |
| `orderBy` | string | no | Sort channels by last modified or creation time. |
| `nextToken` | string | no | Use the next token from a previous response to retrieve the next channel page. |
| `syncToken` | string | no | Retrieve channels updated after the previous synced request. |
| `pinned` | boolean | no | When true, only pinned channels are returned. |
| `joined` | boolean | no | When true, only joined channels are returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": [
        {}
      ],
      "has_more": true,
      "next_token": "string",
      "sync_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | array<object> |  |
| `has_more` | boolean |  |
| `next_token` | string |  |
| `sync_token` | string |  |

## Native endpoint

Through the native Zoho Cliq API, this operation is `GET /channels` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

