# Weberlo: List Channels

Retrieves a list of channels from Weberlo.

```
GET https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/list-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weberlo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weberlo/latest/actions/list-channels?${params}`, {
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
      "adAccountId": "string",
      "adAccountPlatform": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "icon": "string",
      "id": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adAccountId` | string |  |
| `adAccountPlatform` | string |  |
| `createdAt` | date |  |
| `icon` | string |  |
| `id` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Weberlo API, this operation is `GET /channel/list` (base URL `https://connect.weberlo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channels.md) for the provider-specific parameters and requirements.

