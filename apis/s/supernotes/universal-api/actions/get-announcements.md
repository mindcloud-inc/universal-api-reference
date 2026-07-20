# Supernotes: Get Announcements



```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-announcements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-announcements?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-announcements?${params}`, {
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
      "announcedWhen": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "markup": "string",
      "title": "string",
      "youtubeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `announcedWhen` | date |  |
| `id` | number |  |
| `markup` | string |  |
| `title` | string |  |
| `youtubeId` | string |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /announcements/` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-announcements.md) for the provider-specific parameters and requirements.

