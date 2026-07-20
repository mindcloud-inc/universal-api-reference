# Foreplay: Get Brand Analytics

Retrieves brand analytics data from Foreplay.

```
GET https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-brand-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Foreplay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-brand-analytics?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-brand-analytics?${params}`, {
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
| `id` | string | yes | The brand or page identifier to analyze. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_count": 1,
      "carousel": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "dco": 1,
      "dpa": 1,
      "event": 1,
      "image": 1,
      "inactive_count": 1,
      "multi_images": 1,
      "multi_medias": 1,
      "multi_videos": 1,
      "page_like": 1,
      "text": 1,
      "video": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_count` | number |  |
| `carousel` | number |  |
| `date` | date |  |
| `dco` | number |  |
| `dpa` | number |  |
| `event` | number |  |
| `image` | number |  |
| `inactive_count` | number |  |
| `multi_images` | number |  |
| `multi_medias` | number |  |
| `multi_videos` | number |  |
| `page_like` | number |  |
| `text` | number |  |
| `video` | number |  |

## Native endpoint

Through the native Foreplay API, this operation is `GET /api/brand/analytics` (base URL `https://public.api.foreplay.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-brand-analytics.md) for the provider-specific parameters and requirements.

