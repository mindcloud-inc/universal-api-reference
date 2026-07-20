# Recut URL Shortener: List Campaigns

Retrieves campaigns from Recut URL Shortener.

```
GET https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/list-campaigns?${params}`, {
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
      "id": 1,
      "list": "string",
      "name": "Ava Chen",
      "public": true,
      "rotator": "string",
      "views": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Campaign ID. |
| `list` | string | Campaign list URL. |
| `name` | string | Campaign name. |
| `public` | boolean | Whether the campaign is public. |
| `rotator` | string | Rotator URL. |
| `views` | number | Campaign view count. |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `GET /campaigns` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

