# TikHub: Get User Posts

Retrieves TikTok posts for a user from TikHub.

```
GET https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-user-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-user-posts?connectionId=$CONNECTION_ID&secUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "secUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-user-posts?${params}`, {
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
| `secUid` | string | yes | User secUid |
| `cursor` | number | no | Page cursor |
| `count` | number | no | Number per page |
| `coverFormat` | number | no | Cover format |
| `postItemListRequestType` | number | no | Sort type |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |

## Native endpoint

Through the native TikHub API, this operation is `GET /api/v1/tiktok/web/fetch_user_post` (base URL `https://api.tikhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-posts.md) for the provider-specific parameters and requirements.

