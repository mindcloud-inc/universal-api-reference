# Hacker News: Get Poll

Retrieves a poll from Hacker News.

```
GET https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-poll
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hacker News `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-poll?connectionId=$CONNECTION_ID&id=126809" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "126809"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-poll?${params}`, {
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
| `id` | number | yes | Numeric Hacker News item ID. Default: `126809`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "by": "string",
      "descendants": 1,
      "id": 1,
      "kids": [
        1
      ],
      "parts": [
        1
      ],
      "score": 1,
      "text": "string",
      "time": 1,
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `by` | string |  |
| `descendants` | number |  |
| `id` | number |  |
| `kids` | array<number> |  |
| `parts` | array<number> |  |
| `score` | number |  |
| `text` | string |  |
| `time` | number |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Hacker News API, this operation is `GET /item/:id.json` (base URL `https://hacker-news.firebaseio.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-poll.md) for the provider-specific parameters and requirements.

