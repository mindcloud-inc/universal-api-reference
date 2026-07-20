# NewsBlur: List Feed Trainers

Retrieves feed classifiers from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-feed-trainers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-feed-trainers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-feed-trainers?${params}`, {
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
| `feedId` | number | no | Optional feed ID to load classifiers for a single feed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feed_trainers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feed_trainers` | array<object> | Feed trainer data, one entry per feed. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/feeds_trainer` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-feed-trainers.md) for the provider-specific parameters and requirements.

