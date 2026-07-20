# Wistia: Get Current Account

Retrieves the current Wistia account details.

```
GET https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-current-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wistia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wistia/latest/actions/get-current-account?${params}`, {
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
      "channelCount": 1,
      "folderCount": 1,
      "id": 1,
      "mediaCount": 1,
      "name": "Ava Chen",
      "url": "https://example.com",
      "videoLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelCount` | number | The total number of channels in this account |
| `folderCount` | number | The total number of folders in this account |
| `id` | number | Numeric id of the account |
| `mediaCount` | number | The total number of medias in this account |
| `name` | string | Account name |
| `url` | string | Account’s main Wistia URL (e.g. http://brendan.wistia.com) |
| `videoLimit` | number | The account's video limit |

## Native endpoint

Through the native Wistia API, this operation is `GET /modern/account` (base URL `https://api.wistia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-account.md) for the provider-specific parameters and requirements.

