# Hacker News: Get Item Child IDs

Retrieves an item's child IDs from Hacker News.

```
GET https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-item-child-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hacker News `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-item-child-ids?connectionId=$CONNECTION_ID&id=8863" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "8863"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hackerNews/latest/actions/get-item-child-ids?${params}`, {
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
| `id` | number | yes | Numeric Hacker News item ID. Default: `8863`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | array<number> | Ordered child comment IDs for an item. |

## Native endpoint

Through the native Hacker News API, this operation is `GET /item/:id/kids.json` (base URL `https://hacker-news.firebaseio.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-child-ids.md) for the provider-specific parameters and requirements.

