# Feedbin: List Subscriptions

Retrieves a list of subscriptions from Feedbin.

```
GET https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feedbin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feedbin/latest/actions/list-subscriptions?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `since` | date | no | Return subscriptions created after this ISO 8601 timestamp. |
| `mode` | string | no | Use extended to include additional subscription metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "feed_id": 1,
      "feed_url": "https://example.com",
      "id": 1,
      "site_url": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `feed_id` | number |  |
| `feed_url` | string |  |
| `id` | number |  |
| `site_url` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Feedbin API, this operation is `GET subscriptions.json` (base URL `https://api.feedbin.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

