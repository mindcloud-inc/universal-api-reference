# Hacker News: Get Item ID

Retrieves an item ID from Hacker News.

```
GET https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-item-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hacker News `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-item-id?connectionId=$CONNECTION_ID&id=47702791" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "47702791"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-item-id?${params}`, {
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
| `id` | number | yes | The Hacker News item ID. Default: `47702791`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number | The item ID. |

## Native endpoint

Through the native Hacker News API, this operation is `GET /item/:id/id.json` (base URL `https://hacker-news.firebaseio.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-id.md) for the provider-specific parameters and requirements.

