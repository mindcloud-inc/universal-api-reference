# Pinboard: List Post Dates



```
GET https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/list-post-dates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/list-post-dates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/list-post-dates?${params}`, {
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
| `tag` | string | no | Filter by up to three tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Number of bookmarks on that date. |
| `date` | date | Bookmark date bucket. |

## Native endpoint

Through the native Pinboard API, this operation is `GET /posts/dates` (base URL `https://api.pinboard.in/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-post-dates.md) for the provider-specific parameters and requirements.

